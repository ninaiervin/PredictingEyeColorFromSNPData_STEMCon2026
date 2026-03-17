[CLICK HERE](https://mybinder.org/v2/gh/ninaiervin/PredictingEyeColorFromSNPData_STEMCon2026/HEAD)

# Predicting Eye Color from SNP Data Using ML

## Please Follow These Steps for STEM Con 2026:

1. Login to a computer
2. Navigate to this page (You did it!)
3. Download the .ipynb file and the .csv file
4. Open and login to Google Colab using your google account (https://colab.research.google.com)
5. Upload the .ipynb file as a new project in Google Colab
   <img width="628" height="492" alt="image" src="https://github.com/user-attachments/assets/dd4d4a39-2969-430d-91ff-1d282def5023" />
7. Upload the .csv file in that project under the files tab on the left
   
   <img width="268" height="276" alt="image" src="https://github.com/user-attachments/assets/28c73436-757d-4b2d-ab27-975d9263749a" />

## Dataset
 ChrisTho23. (2024). Gen2PhenMini [Data set]. GitHub. https://github.com/ChrisTho23/Gen2PhenMini


 ****
**Step 6: Improve the Base Linear Classifier**
****

Below are different factors that affect how our model will learn. These are pre-set during training and require the model to be retrained each time a value is changed.

**C** &rarr; tells the model how strictly it should try to get every training example right.
  * If C is big, then you are very strict. This can lead to memorizing training data and not learning the true pattern of the data.
  * If C is small, then you are more relaxed about getting things wrong. This can lead to not trying hard enough to learn how to predict eye color.
  * You want to find a happy middle where the model cares about learning how to solve the problem.

**Penalty** &rarr; Stops the model from getting too wild or overthinking too much.
  * None = No rules. Do whatever you want.
  * L2 = Look at everything, but don't look at any one thing too much.
  * L1 = Don't look at everything only look at the important things.
  * Elastic Net = Do a balance between L1 and L2.

**tolerance** &rarr; How patient we should be before saying "good enough".
  * Small tolerance = Be a perfectionist. Don’t quit early.
  * Large tolerance = Good enough is good enough.

**class_weight** &rarr; tells the model how much attention it should give to each class (each eye color) when learning.
  * None = Every class counts the same.
  * Balanced = Give rare classes extra volume so they’re heard.

**solver** &rarr; The method the computer uses to figure out the best line or boundary. (*note - not all penalties work for all solvers!*)
  * lbfgs = calm and steady problem solver. (must use L2 or None penalty)
  * sag/saga = great for big datasets; saga is the most flexible. (must use L2 or None penalty for sag. Must use L1, L2, Elastic Net, or None penalty for saga)
  * newton cg/newton-cholesky = intelligent big step solver. ( must use L2 or None penalty)

**max iteration** &rarr; A limit on how long the model is allowed to keep trying to learn.
  * Too few iterations = turning something in before it is finished.
  * Too many iterations = won't make the model smarter it will just take longer.

**warm start** &rarr; Tells the model whether to start learning from scratch or continue learning from where it left off.








