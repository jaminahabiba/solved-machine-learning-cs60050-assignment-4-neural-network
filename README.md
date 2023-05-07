Download Link: https://assignmentchef.com/product/solved-machine-learning-cs60050-assignment-4-neural-network
<br>



In this assignment you will build a multilayer neural network and classify whether a given message is SPAM or HAM (non-spam). The dataset has 5574 messages, each annotated as SPAM or HAM. The dataset can be downloaded from: <a href="https://drive.google.com/file/d/1o-ek6ZLVUnpdT4on74DTNVMKa4e_ctMU/view?usp=sharing">https://drive.google.com/file/d/1o-ek6ZLVUnpdT4on74DTNVMKa4e_ctMU/view?usp=sh </a><a href="https://drive.google.com/file/d/1o-ek6ZLVUnpdT4on74DTNVMKa4e_ctMU/view?usp=sharing">aring</a>

<strong> </strong>

<strong>                                     </strong>

<strong><u>Preprocessing:</u></strong>

<ol>

 <li>Break each message into tokens (any sequence of characters separated by blanks, tabs, returns, dots, commas, colons and dashes can be considered as tokens)</li>

 <li>Remove a standard set of English stopwords, e.g., the set available at <a href="https://gist.github.com/sebleier/554280">https://gist.github.com/sebleier/554280</a></li>

 <li>Apply Porter stemming.</li>

</ol>




Consider 80% of the dataset (randomly selected) as training data, and the rest 20% as test data.




Compute the set of distinct tokens in the dataset (denoted as V). Represent each message as a (|V| x 1) vector, where each entry <em>j</em>​ ​is 1 or 0 depending on whether token <em>j</em>​ is present in the message. This is your input representation and should be fed into the input layer. This representation is usually referred to as ‘one hot encoding’. <em>If</em>​<em> you cannot manage a network with all distinct tokens, you can consider the most frequent 500 tokens only.</em>

<strong> </strong>

<h1>PART 1</h1>

Build a neural network with 1 hidden layer and perform the text classification task.




Neural network specifics:

<ol>

 <li>No of hidden layers : 1</li>

 <li>of neurons in hidden layer: 100</li>

 <li>Non-linearity in the layer : Relu</li>

 <li>Use 1 neuron in the output layer. Use a suitable threshold value, and classify a message as SPAM if the score is above threshold or HAM if it is below threshold.</li>

 <li>Optimisation algorithm : Stochastic Gradient Descent (SGD) <strong> </strong></li>

 <li>Loss function : categorical cross entropy loss</li>

</ol>




The function Relu is defined as : f(x) = max(0,x)

It’s derivative : f’(x) = 0, if x&lt;=0

= 1, otherwise

You should define the relu function and its derivative. Do not use any inbuilt library for this.




Do a random initialisation of the weights. Use learning rate 0.1.

<strong> </strong>

<strong><u>Implementation</u></strong>​:

Have the following modules/functions in your code :

<ol>

 <li>Preprocess: Use this module to preprocess the data and divide into train and test.</li>

 <li>Data loader : Use this module to load all datasets and create mini batches</li>

 <li>Weight initialiser : This module should initialize all weights</li>

 <li>Forward pass: Define the forward() function​ where you do a forward pass of the neural network.</li>

 <li>Backpropagation : Define a backward()​ function where you compute the loss and do a backward pass (backpropagation) of the neural network and update all weights.</li>

 <li>Training : ​ Implement a simple minibatch SGD loop and train your neural network, using forward and backward passes. Continue the experiment till training error becomes very low. Finally it should print the accuracy after training.</li>

 <li>Test: To test the learned model weights on the test set.</li>

</ol>







<h1>PART 2</h1>

Build a neural network as follows:

<ul>

 <li>of hidden layers = 2</li>

 <li>of neurons in the two hidden layers ​<u>should be taken as command-line</u> <u>arguments</u><u>​</u>.</li>

 <li>of neurons in the output layer = 2</li>

</ul>




Use ​<u>sigmoid function</u><u>​</u> for non-linearity in this part. Do not use any inbuilt python library.




Use ​<u>softmax function</u>​ in the output layer. Softmax will convert the outputs of the neural network in each neuron to the probability of a message being SPAM or HAM. Based on the higher probability you will classify a message to its class. You can see <u>​</u><a href="https://www.youtube.com/watch?v=LLux1SW--oM">this video</a>​ for implementing the softmax function




Define the forward and backward passes accordingly.

<strong> </strong>

The implementation should have the same functions as defined in Part 1.







<strong> </strong>

<h1>Report</h1>




For both parts, report :

<ol>

 <li>Training set error over number of epochs</li>

 <li>Test set errors over number of epochs</li>

 <li>Final Test set accuracy</li>

</ol>




Submission instructions




For each part, you should submit the source code and all result files. Write a separate source code file for each part. ​<strong>You should include a README file describing how to execute each of your codes</strong>​, so that the evaluators can test your code.




<strong>You can use C / C++ / Java / Python for writing the codes; no other programming language is allowed. </strong>​<strong>You cannot use any library/module meant for Neural Networks or Machine Learning or Deep Learning</strong>​<strong>. You can use libraries for other purposes, such as formatting and pre-processing of data, but </strong><strong>NOT</strong>​<strong> for the ML part</strong><strong>.</strong>​<strong> Also you should not use any code available on the Web. </strong>​<strong>Submissions found to be plagiarised or having used ML libraries will be awarded zero marks for all the students concerned. </strong>




All source codes, data and result files, and the final report ​<strong>must be uploaded via the course Moodle page, as a single compressed file (.tar.gz or .zip)</strong>​.​ The compressed file should be named as: <strong>{</strong>​ <strong>ROLL_NUMBER}_ML_A4.zip or {ROLL_NUMBER}_ML_A4.tar.gz </strong>

Example: If your roll number is 16CS60R00, then your submission file should be named as 16CS60R00_ML_A4.tar.gz or 16CS60R00_ML_A4.zip


