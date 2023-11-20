# Speech-Sentiment-Detection
Automatic Speech Recognition - Course Project <br />
Supervisor = Prof Preethi Jyothi <br />
Dataset = HyperValleyBank <br />
-> Implemented a speech sentiment detection model using the pre-trained SpeechBrain CRDNN model <br />
-> Achieved an accuracy of 78% by fine-tuning the encoder of the pre-trained model within few epochs only <br />


Task0)  <br />
Pretrained Model result:  <br />
1) WER = 75.84  <br />
2) SER = 87.8  <br />

Three types of common errors found in predicted sentence:  <br />
1) Few words are same, But sentence is entirely different meaning:  <br />
	21331: 63.63636363636363  <br />
	True: HELLO THIS IS HARPER VALLEY NATIONAL BANK MY NAME IS MICHAEL  <br />
	Pred: OH IT'S THE PAPA VALLEY NATIONAL BAY I NAME IT MICHAEL  <br />
2) Words(belonging to truth) are repeated:  <br />
	21423: 425.0  <br />
	True: MY NAME IS DAVID  <br />
	Pred: AND DAVID DAVID THE DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID DAVID  <br />
3) No word is same:  <br />
	542: 100.0  <br />
	True: WHAT IS THE COMPANY ADDRESS  <br />
	Pred: WON'T BE ACCOMPANYED  <br />

Changes in train.yaml:  <br />
1) lr=0.5  <br />
2) label_smoothing=0.01  <br />

New result:  <br />
1) Train Loss = 0.489  <br />
2) Valid Loss = 0.571  <br />
3) Valid CER = 87.36  <br />
4) Valid WER = 84.87  <br />
5) Test WER = 31.12  <br />
6) Test SER = 54.0  <br />
 <br />
Task 1) Accuracy on testing set (dev.txt) - 78
