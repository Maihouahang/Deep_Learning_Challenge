# Deep_Learning_Challenge

#### Overview of the analysis:

This analysis is about training a deep learning model to predict whether an organization will receive funding. The goal is to help Alphabet Soup Charity make better funding decisions.

#### Results:

* What variable(s) are the target(s) for your model?
  * The target variable is "IS_SUCCESSFUL", which tells us whether an organization got funding (1 = Yes, 0 = No).
* What variable(s) are the features for your model?
  * Features are the pieces of information used to predict the outcome. The following below are what the model uses to guess if funding will be approved:
    * Application type
    * Organization type
    * Income amount
    * Special considerations
* What variable(s) should be removed from the input data because they are neither targets nor features?
  * I removed the EIN, which is a tax ID number.
  * I also removed the NAME, which is the organization’s name. This doesn't affect funding decisions
 
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * For the AlphabetSoupCharity.ipynb file, I did the first layer as 16 neurons (ReLU activation), second layer as 16 neurons (ReLU activation), and the output layer as 1 neuron (Sigmoid activation, which gives a probability). This was just a random amount that I selected to first start off and see what the results I would get would be. I got an accuracy of 72%.
  * Were you able to achieve the target model performance?
    * No, I was not able to acheive the target model performance of an accuracy higher than 75%.
  * What steps did you take in your attempts to increase model performance?
    *  So I tried a few times in the AlphabetSoupCharity_Optimization.ipynb file to see if I could acheive a higher accuracy of 72%.
      *  First attempt: I thought maybe it was because I needed to add more neurons to to get a higher accuracy. I had the first layer as 30 neurons, second layer as 30 neurons, and the output layer remained as 1 neuron. The accuracy was still 72%.
      *  Second attempt: I thought maybe I need to add more layers and even more neurons to get a higher accuracy. I had the first layer as 50 neurons, second layer as 50 neurons, third layter as 50 neurons, and the output layer remined as 1 neuron. However, the accuracy still remained at 72%.
      *  Last attempt: I thought maybe if the issue is not about adding more neurons but having more epochs. So I mixed up the numbers of neurons per layer to be different. The first layer had 50 neurons, second layer had 25 neurons, third layer had 14 neurons, and the output layer remained as 1 neuron. I increased the epochs from 100 (which was what it was for in the first and second attempt) to 300. However, even after trying all, the accuracy still was 72%.

#### Summary:
The deep learning model was able to make predictions, but it wouldn't be considered accurate enough for predicting whether an organization will receive funding or not. Even after trying to tune of many parameters, like number of layers and neurons, it was hard to get an accuracy of higher than 72%. Other models like Random Forest could work better for this type of problem. One reason why I say that is because the dataset has a lot of categorical variables (e.g., Application Type, Organization Type). Random Forest handles categorical variables better without needing as much preprocessing as deep learning.

## References:

IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/Links to an external site.

OpenAI. (2023). ChatGPT (Mar 14 version) [Large language model]. Accessed on March 2025. I used this website to help me with how to create a list of application types to be replaced. It specifically helped me in how to use the method: index.tolist(). This is step 5 on my AlphabetSoupCharity.ipynb file. Retrieved from https://chat.openai.com/chat
