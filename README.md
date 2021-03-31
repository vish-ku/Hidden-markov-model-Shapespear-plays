# Hidden-markov-model-Shapespear-plays
This is the second project of machine learning, where we use Hidden Markov Model to generate and predict words. 

## Objective
Use hidden Markov model to generate and predict text by training the data on a play by Shakespear.
In this project I chose the play 'Hamlet' which has approximately 6000 unique words.

## Hidden Markov Model
This is a Markov Model, where we assume the observation are related to a set of Hidden variables/Latent varibles and it is the latent variable satisfy a first order markov chain rather than the observation. The concept of considering latent variables is similar to that of the Expectation maximization algorithm, which was done in the first project. 

All Hidden Markov model are completely described by a set of parametes: an initial parameter $\pi$, which describes the initial distribution of the latent variables, a transition probability matrix, which describes the probability of next latent variable given a latent variable and an emission probability, which describes the probability that a given variable is observed form the latent variable.

However the main difficulty in implimentaion of the HMM is to optimize the parameters. One of the algorithm that helps us to optimize them is the Baum-Welch algorithm or the forward-backward algorithm. This algorithm is highly depends on the parameters used to initiate the algorithm. Once initialized it converges to a locally optimum parameters. ( The best parameters could be something different, it will depend on the initial values.)

Another problem that arises in the HMM is that given a sequence of observations, how can we find the best possible sequence of latent variables? This is addressed by the Viterbi algorithm. The Viterbi algorithm reduces the computational cost to linear from exponential possibilities. 

## Implementaion

In this project, I have implemented the Baum- Welch algorithm for optimizing the parameters of the model and used the model to generate texts of given length. 
I model is trained on the play 'Hamlet' by Shakespear. The play has about 6000 unique words. The model was trained with 7 latent variables, one may think of them as parts of speech in the english language, like verb, noun, etc. The model ran pretty fast it took about 30 sec to train the model.


To predict a word following a given a sentence, I used the Viterbi algorithm. Using the algorithm, we find the best possible sequence of latent variables depending on the given words, and then the next latent variable is chosen from the transition probabilities, following which a word is chosen from its emmision probabilities.

## Results

The results are recorded in the python notebook. 





