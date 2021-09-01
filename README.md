# COVID-19 Tweet Natural Language Processing
![image](https://user-images.githubusercontent.com/69719467/121576299-3ac41980-c9f6-11eb-9cb9-41bb91f687ba.png)

# Lisa DiSalvo                        
ldisalvo@arcadia.edu 
Arcadia University
Computer Science & Math Department
Class of 2023, Computer Science Major

# Mentor Junyi Jessy Li
https://jessyli.com/
jessy@austin.utexas.edu
Assistant Professor
Department of Linguistics
The University of Texas at Austin


In collaboration with Jessy Li From the University at Texas Austin, for the DREU 2021 program, I will be delving into Natural Language Processing in relation to COVID-19 related tweets.


# Week One/Week Two - Beginning Steps

Introduction to Natural Language Processing. My Mentor and I discussed what types of Projects I would be interested in.
After Reviewing all of the projects, I decided to pursue a project that would be built on, originally the Hurricane Perception project (https://www.aclweb.org/anthology/2020.acl-main.471/), we will now be improving this program to detect information from COVID-19 Related tweets. Reading through the HurricaneEMO paper, I believe we will attain our data the same way data was retrieved for HurricaneEMO : 
We randomly sample 5,000 tweets each for annotation from the filtered datasets for Harvey, Irma, and Maria; in total, this yields 15,000 annotations.
We request workers on Amazon Mechanical Turk
to label tweets with a list of Plutchik-24 emotions.
Furthermore, to enable fine-grained emotion analysis, we do not crowdsource Plutchik-8 emotions
directly. We require that workers reside in the US
and have completed 500+ HITs with an acceptance
rate ≥ 95%. Each HIT is completed by 5 workers (Li, Desai, Caragea)

The first few steps to my data process is annotating tweets like so:

![image](https://user-images.githubusercontent.com/69719467/121575761-bbcee100-c9f5-11eb-95b0-8f6d9e9f5cdb.png)

Then, I am expected to do some more annotating of tweets, but in a more computational manner. I am looking to tokenize words and count the frequency of words in the given tweet dataset. I could also put the words into a data frame and use python pandas to count the frequency of certain buzz 'emotion' words in a tweet dataset. Through the data found in the computerized task, we can make conclusions on the overall 'emotion' attached to COVID-19 related tweets. We can also categorize tweets on what overall emotion they portray. 
In Weeks Three & Four I can expand on my task findings. Overall, these two weeks really focused on introducing the project, introducing myself to my project partners and trying to truly understand what we are looking to do with our dataset and how we can accelerate progress into possibly publishing a paper on COVIDEmo

# Week Three/Week Four

My Mentor Introduced me these weeks to my research collaborates Chau Pham and Cornelia Caragea. I am shadowing Chau Pham, as she was in my position a year or two ago mentoring with Dr. Li as a DREU student. 
Essentially, I have to understand workflows, and get a secure handle of Amazon Mechanical Turk to gather a dataset.

Our project involves scraping Twitter API for COVID-19 Related tweets. Then, with these tweets we create a qualification task on Amazon Mechanical Turk. We create this task on AMT to gather an annotated dataset in order to preform qualification tasks such as using a BERT model on our data, and preforming more qualification tasks on our data alike the tasks performed for the HurricaneEMO dataset. 

Alot of my work this week involved lots of annotating tweets. I had to go through about 80+ tweets and annotate them based on emotion. We did this multiple times, and even annotated multiple emotions to one tweet in order to gather a good sense of what the tweet was. Along with Chau, the annotating was very straightfoward and easy, and we found that Chau and I annotated similarly. However, Chau and I, while OUR annotations are similar, the average MTurker's annotations differs from ours. I believe that our annotation differences are due to the fact that Chau and I are in similar life positions. We are both female, university students majoring in STEM. We cannot be sure what the average education level is for an Amazon Turker, so therefore that is why I believe our annotations differ from the turkers. We also noticed that Amazon Turkers seem to somewhat annotate lazier. The first round of annotations were not the best, which therefore led to Chau having to experiment, and strategeically choose the tweets we submit as the HIT task for Turkers. Like any research group, we want well annotated data, and a dataset of difficult to annotate tweets would possibly cause discrepancies in the data.

Screenshots of my annotations: 

This is what our final annotation looked like. These are the tweets that will be offered to Turkers in order to annotate. 
![Screenshot 2021-07-05 113611](https://user-images.githubusercontent.com/69719467/124495627-57016f00-dd86-11eb-9e8b-2606f28aacf3.png)


This is what the first few annotations looked like. It's simple, you assign an emotion to a tweet. 
![b85cf7e5deb4396658a96ffa3b11a2d6](https://user-images.githubusercontent.com/69719467/124495897-b495bb80-dd86-11eb-9ce4-bfc215270281.png)




# Week Five/Six

We began discussing politics, and stances in certain tweets. It is no secret that COVID-19 is a highly publicized and politicized disease. 

Cornelia mentioned that she was collaborating with Kansas State University, and in her ACL paper, she is thinking of annotating stances in politically fueled tweets. We discussed the possibility of annotating stances in our paper and also possibily annotating whats 'between the lines' in some tweets. We as a group collectively disagreed on annotating political stances as this seemed to be an expansion of the project. We wanted to keep to annotating emotions. However, I made a point that political stances would reveal themselves if we inserted the heavily political COVID-19 tweets for turkers to annotate. In a set of about 10 questions possibly one or two tweets would be 'political' anchor tweets. Based on user response, we can safely assume someone's feelings in relation to COVID-19 and their political stance. Reactions to poltiical fueled tweets vary from person to person, and based on a negative or positive reaction we could completely see the proportion of Turkers with more right leaning stances as opposed to left leaning stances.

# Week Seven/Eight 
This week was mostly uneventful. What was really focused on was making sure new batches were pushed on Amazon Mechanical Turk in order to receive more annotations. Therefore, once annotations are done, the actual modeling and analysis can be done 

# Week Nine/Ten

This week focused on learning to model according to the HurricaneEmo paper. I took an in-depth look at shrey’s HurricaneEmo GitHub repo and tried to model for our CovidEmo set using Chau’s CovidEmo datasets on GitHub. I did not know if the data files in that GitHub were up to date but I did modeling on that anyways. Collaboration with chau on this project made things much easier as we both encountered compiling errors and gave each-other advice on how to fix it. In order to run the HurricaneEmo modeling, I first had to download the code from HurricaneEmo  and modify it to work on CovidEmo’s data . For example. I had to go in and manually change the name of the emotions being tested on in the code as HurricaneEmo has a different set of emotions being measured. Secondly we also had to make some minor adjustments so the code would actually run. These adjustments included indentation errors and things like fixing errors that compile with code (adjusting code to work with our specific dataset). When getting my code to run, I had to use commands such as: 

python train.py --model "bert" --ckpt "ckpt/bert.pt" --tokenizer "bert" --bert_model "bert-base-uncased" --batch_size8 --grad_step2 --epochs 3 --lr 2e-5 --w 0 --test_path "E:\Downloads\aSafeHaven\letsTakeItEasy\solidstatesociety\EmoNet-main\data\large_dev\binary\anticipation_test.csv" --train_path "E:\Downloads\aSafeHaven\letsTakeItEasy\solidstatesociety\hurricane-master\datasets_binary\optimisim_train.csv" --valid_path "E:\Downloads\aSafeHaven\letsTakeItEasy\solidstatesociety\EmoNet-main\data\large_dev\binary\anticipation_dev.csv"
[11:32 AM]
had to also tweak each command for every emotion I tested on and it was initially very difficult as I had to find each file path for the emotion label files. In the end, it paid off as I received the following results 
    
            ANGER   ANTICIPATION    DISGUST FEAR    JOY     SADNESS SURPRISE    TRUST  
    BERT    0.73            0.85    0.73    0.76    0.85    0.78        0.89    0.86

These results very somewhat outlandish as they are surprisingly high. However, the magic of collaboration allowed for my peers to test on their own machines and receive better more accurate results 

# Week 11

This is supposed to be the end of my DREU experience I believe, but I will continue to further collaborate with the team to try and release our paper to research conferences. It will be my first time ever helping prep a research paper for these types of events so it should be an enriching experience. I believe using Bert and Roberta to train and model the past week is great practice for me because I have an internship coming up that involves creating a pipeline and using BERT models. I believe that through my DREU experience I learned to collaborate with a team and learn workflow practices with my peers. I really enjoyed meeting weekly and in each meeting we always had at-least one hour or more to talk about a ton of topics pertaining to our paper.
 
Here is the link to my Final Report: 

(https://docs.google.com/file/d/1qD1toPK3e31-omVvPJtB7ijEfsJ-j1X3/edit?usp=docslist_api&filetype=msword)

