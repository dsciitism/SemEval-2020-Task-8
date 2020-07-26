# Bi-Fusion Techniques for Deep Meme Emotion Analysis

DSC IIT-ISM at SemEval-2020 Task 8: Bi-Fusion Techniques for Deep Meme Emotion Analysis

Authors: Pradyumna Gupta, Himanshu Gupta and Aman Sinha  
(Accepted at SemEval-2020 Workshop, collocated with COLING'2020)

Keras version: 2.3.0  
Tensorflow version: 2.2.0

## Why memes matter?

* Social media is becoming increasingly abundant in memes which are mostly derived from news, popular TV shows and movies making them capable of conveying ideas that the masses can understand readily.
* Although they are mostly for amusement and satire, memes are also being used to propagate controversial, hateful and offensive ideologies.
* Since it is not feasible to manually inspect such content it is important to build systems that can process memes and segregate them into appropriate categories.

## Tasks Involved

* Task A involves classifying the sentiment of an internet meme as positive, negative or neutral.
* Task B is the multilabel classification of a meme into 4 categories viz. sarcastic, humorous, offensive
and motivational.
* Task C is to quantify, on a scale of 0-3 (0 = not, 1 = slightly, 2 = mildly, 3 = very), the extent of
sarcasm, humor and offence expressed in a meme.

Detailed information about the task and dataset can be found at https://competitions.codalab.org/competitions/20629

## Models Used

We use a combination of state-of-the-art model architectures and adapt them for processing multimodal memes through transfer learning while also training models from scratch for comparison.
* Text Models: BiLSTM, RoBERTa
* Vision Models: AlexNet, ResNet

## Modality Fusion
![](/Fusion_Diagram.png)

We explore three modality fusion techniques:\
a) Early Fusion \
b) Gated Multimodal Unit (GMU) \
c) Late Fusion

## Results

Overall, the RoBERTa+ResNet model with Early Fusion has the best performance for Task A and Task B with F1 scores 0.357 and 0.510 respectively. The same model using the Late Fusion strategy has the best F1 score of 0.312 for Task C.
