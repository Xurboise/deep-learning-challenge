Overview of the analysis: Explain the purpose of this analysis.
The foundation "Alphabet Soup" wants a tool to help to select applicants for funding. They require a binary classifier to predect  if applicants will be successful if funded.


Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?
"IS_SUCCESSFUL" column from the application_df was my target variable.
What variable(s) are the features for your model?
Every column but the previously mentioned, got this by dropping that said var from the original dataframe.
What variable(s) should be removed from the input data because they are neither targets nor features?
"EIN" column were removed, as it didn't impact the behavoir of the model.

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
In the Optimized version of the model, I used 3 hidden layers each with multiple neurons which increased the accuracy to <75% to 79%. The Initial model had only 2 layers. Although the number of epochs did not change between the Initial and the Optimized Model, adding a 3rd Layer increased the accuracy of the model.

Were you able to achieve the target model performance?
Yes, from 72% to about 79%.

What steps did you take in your attempts to increase model performance?
Only dropped the EIN column, but only names that appeared over 5 times were considered. Added a 3rd activation layer, which boosted the accuracy above 75%. Instead of both 2nd and 3rd layers being sigmoid, the 2nd used tanh and the 3rd sigmoid. This boosted the accuracy above 79%.

Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Optimizing the model brought the accuracy above 79%. Applicants have an about 80% chance of being successful if the name on the application appears more than 5 times, the type of the application is T3, T4, T5, T6, T19, and if their classification is C1000, C1200, C2000, C2100, and C3000.