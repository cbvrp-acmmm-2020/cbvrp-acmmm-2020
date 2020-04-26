# Cancellation: Content-based Video Relevance Prediction Challenge

<font color=red>Due to the pandemic of COVID-19 influence, Hulu decided to cancel the CBVRP challenge. We really appreciate your interest in our challenge and sorry for the inconvenience to you. We hope we can find a chance to continue the CBVRP challenge after this difficult period.</font>

### @ACM Multimedia 2020, Seattle, United States
![](hulu_logo.png)

**(This challenge is fully sponsored by Hulu.)**

## Motivation

Video relevance computation is one of the most important tasks for personalized online streaming service. Given the relevance of videos and viewer feedbacks, the system can provide personalized recommendations, which will help the viewer discover more content of interest. In most online services, the computation of video relevance table is based on the viewers' implicit feedback, e.g. watch and search history. The system analyzes the viewer-to-video preference and computes the video-to-video relevance scores using collaborative filtering based methods. However, this kind of method performs poorly for “cold-start” problem - when a new video is added to the library, the recommendation system needs to bootstrap the video relevance score with very little historical viewer feedbacks. One promising approach to solve the “cold-start” problem of new items is analyzing video content itself to predict the relevance score, i.e. predicting the video-to-video relevance by analyzing the metadata of video such as keyframes, audio, subtitles. With the relevance score, we can provide better recommendations for our viewers. 

## Background

CBVRP challenge has been held during the last three years (ICIP2017, ACM Multimedia 2018, ACM Multimedia 2019). It has obtained more and more attention from both academic research community and industry. For the CBVRP challenge held in ACMMM2019, there are over 200 participants, and 12 teams submitted their results. (https://github.com/cbvrp-acmmm-2019/cbvrp-acmmm-2019). A big advancement on this task has been made by the winner teams. The success of CBVRP challenge demonstrates that video relevance prediction based on content understanding is a very valuable and meaningful research task. Meanwhile, we realized that video understanding, especially for long video (e.g. movies and TV series) is a very challenging and underexplored task. There is still a lot of efforts to be made to facilitate the development in this task.

In order to support sustained and substantial progress in the state of the art on video representation and recommendation, Hulu continuously holds CBVRP challenge in ACM Multimedia 2020 with better refined tasks and more data.  

## Tasks and Data

As is known, content-based video relevance prediction is a very challenging and demanding problem. The critical part of the solution is how to leverage multimodal information and metadata of video to explore the video content. Establishing a descriptive as well as discriminative video representation model plays an important role in this task. Hence, in order to further investigate video relevance using multimodal information, there are two tasks in CBVRP challenge this year.

### Task 1

This task is dedicated to explore how to leverage multimodal information for video relevance prediction. Participants are supposed to judge whether two sets of video clips belong to the same video. Given this large long video relevance dataset, it may be possible to learn powerful video representations that transfer to different video tasks.

#### Data

- A sample:  (*[clip<sub>a<sub>1</sub></sub>, clip<sub>a<sub>2</sub></sub>, ...., clip<sub>a<sub>M</sub></sub>], [clip<sub>b<sub>1</sub></sub>, clip<sub>b<sub>2</sub></sub>, ...., clip<sub>b<sub>N</sub></sub>], label*)
    - A clip is corresponding to a shot or a scene in the video
    - For a clip, we will give 2 types of features, conveying multimodal information.
        - Visual feature: a frame feature obtained from the frames of the clip
        - Audio feature: an audio feature extracted from the audio track of the clip
     All the features are extracted using pre-trained CNN models. 
- *label* indicates whether the two sets of clips are from the same video or not.

#### Evaluation

AUC (Area Under Curve) will be used as evaluation metric.

### Task 2

The main task of this challenge is to solve the “cold-start” problem of new items. According to the viewer behavior history and the video content, participants need to predict the viewer click-through behavior on new TV series or new movies. The viewer feedbacks have been cleaned to avoid any privacy issues. Instead of delivering original video content, audio and visual features are extracted from the video and are delivered. 

#### Data

Data is composed of two parts, viewer records and features of video content. As for viewer records, a data sample is a viewer record. For example, a record “*Show<sub>1</sub> , Show<sub>2</sub> , ... , Show<sub>N</sub>  ->  Show<sub>N+1</sub>*” means a viewer has watched *N* shows in a time sequence and then we recommend *Show<sub>N+1</sub>* to the viewer. If the viewer clicked *Show<sub>N+1</sub>*, we consider this record as a positive sample, otherwise it is a negative sample. A show is represented by a set of clips. The concept of clip is the same as task 1. The features extracted for each clip is the same as task 1. There are respectively a training set, a validation set and a test set. In the test set, we will give a bunch of viewer records. Participants need to calculate a probability score indicating how much probably the viewer will click the TV series/movie we recommend. The training set and validation set will be released to participants after registration. The details of the dataset are given as follows.

|           |   Target Shows    |   Records   |
| --------- |:-----------------:|:-----------:|
|   Train   |   3,944           |  11,754,821 |
|   Val     |     361           |   1,021,495 |
|   Test    |     405           |   1,004,532 |


#### Evaluation

AUC (Area Under Curve) will be used as evaluation metric.

## Registration

To register for the challenge and get access to the dataset, please complete the [Online Agreement Form](https://freeonlinesurveys.com/s/WK0gbfZC). We will send you the download instructions by email after the challenge data available date (Apr. 1, 2020). 

## Submission

After the test data is released, participants can submit the results **3 times a week**. 

The participants should send the results to cbvrp-acmmm-2020@hulu.com. After receiving the submission, we will evaluate the results and send the feedback to the participants by email.


## Schedule

|        Date       |                  Event                  |
| ----------------- |:---------------------------------------:|
|   Apr. 10, 2020    | Registration open                       |
|   Apr. 15, 2020   | Release training and validation data    | 
|   May 18, 2020    | Release test data                       |
|   Jun. 29, 2020   | Deadline for final result submission    |
|   TBD             | Deadline for paper submission           |

The registration is open until Jun. 29, 2020 (the deadline for final result submission).

## Prizes

The total reward is $2,000 USD for each task including the taxable amount, which will be fully sponsored by Hulu LLC. The number of winners will depend on the number of participants and the quality of the results. The organizers reserve the complete right in the final judgement and decision.

## Organizers

Peng Wang (peng.wang@hulu.com) Hulu LLC.\
Yunsheng Jiang (yunsheng.jiang@hulu.com) Hulu LLC.\
Chunxu Xu (chunxu.xu@hulu.com) Hulu LLC.\
Xiaoran Xu (xiaoran.xu@hulu.com) Hulu LLC.\
Jiarui Yang (jiarui.yang@hulu.com) Hulu LLC.\
Xiaohui Xie (xiaohui.xie@hulu.com) Hulu LLC.

## Contact

If you have any question, please send an email to cbvrp-acmmm-2020@hulu.com.
