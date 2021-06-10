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
In Weeks Three & Four I can expand on my task findings. 
