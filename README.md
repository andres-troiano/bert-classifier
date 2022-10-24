# BERT classifier

## 1. Business problem
When calling overdue clients for collection, sometimes the registered phone number is outdated. This can happen when the client moves to a new home, changes jobs, or the line is taken down and reassigned by the phone company to a new client. In some cases agents keep calling outdated phone numbers, wasting valuable time and creating friction for the called party, who repeatedly informs of the misunderstanding.

## 2. Goal
The goal of this project is to classify phone call conversations into two classes, identifying those cases when the called party informed an outdated/incorrect phone number. Said class is labeld as "positive", while normal conversations are labeled as "negative".

## 3. Approach
A pretrained BERT model was fine-tuned for this binary classification task. The specialized training was performed on transcriptions of conversations, made using Amazon Textract. The base model was BETO, a cased Spanish BERT model. This choice was made because the conversations were in Spanish.

Previously this pretrained BERT model had been fine-tuned with our data for the general tasks, i.e, before training for classification. These tasks are Masked Language Modeling (MLM) and Next Sentence Prediction (NSP). There are two notebooks on this repository, with the only difference being that one trains for classification starting from the base model (BETO), while the other one starts with BETO fine-tuned for our data.

## 4. Results
The model performed extremely well, with a general accuracy of 96% using the base model, and 97% using the fine-tuned version.