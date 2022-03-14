# NLP-Autograder-test

In this project we are creating a simple Python notebook that uses BERT tokenizer to quickly find the "most" correct answers to a question.

The question we are using as a test is "What is the difference between supervised and unsupervised machine learning?"

Instead of using a question - answer method we are using some correct answers (written differently) as clusterring center to benchmark all the other questions against them.

With the correct answers, we are also using 9 answers that are not relevant to the question but have a similar structure since they are meant to explain the differences between similar concepts. These questions are used to test if BERT from_pretrained can fully capture the semantics and ignore the similarity of the text structures as well as the use of similar words ("The main difference", "the main distinction", e.t.c). The two final answers are trick-correct answers, they are essentially the answers that a completely unprepared but bold student would give to try and trick the examiner into passing.

The project consists of vectorizing the questions using a BERT tokenizer from Hugging Face. Then we are using two dimensionality reduction techniques (PCA and t-SNE) to visualize the results and see how well the answers are seperated. As we can see from both results there are certainly possibilites of clusterring since we can clearly generate decision boundaries.

Finally, we create a method to find the center of the correct answers and we mesure the vector distance from this center. In the final plot we can see a clear distinction between the distance of the correct and incorrect answers that can be used to seperate the submissions to passing and not. 
