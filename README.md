# Bert classifier

## 1. Business problem
When calling overdue clients for collection, sometimes the registered phone number is outdated. This can happen when the client moves to a new home, changes job, or the line is taken down and reassigned by the phone company to a new client. In some cases agents keep calling outdated phone numbers, creating friction with the person at the other end of the line, who repeatedly inform of the misunderstanding, and wasting valuable time.

## 2. Goal
The goal of this project is to classify phone call conversations into two classes, identifying those cases when the called party informed of an outdated/incorrect phone number. We call that class "positive". Normal conversations are labeled as "negative".

## 3. Approach
A pretrained BERT model was fine-tuned for this binary classification task. The specialized training was performed on transcriptions of conversations, made using Amazon Textract. The base model was BETO, a cased Spanish BERT model (the conversations were in Spanish).

## 4. Results
The model performed extremely well, with a general accuracy of 97%

## 5. Impact
## 6. License
## 7. Contact
## 8. Acknowledgements