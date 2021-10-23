# machine_learning_trading_bot
combining algorithmic trading skills with existing skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.


### Step 1: Tune the training algorithm by adjusting the size of the training dataset. 

## What impact resulted from increasing or decreasing the training window?

As the training windows increased the precision of the -1 class declined while the 1.0 class statyed relatively the same. Based on the higher recall, it seems that the model (based on the training data) is better at predicting the 1 class than the ?1 class as the ending period increased.

# Training data with an offset of 3 months

            precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

# Training data with an offset of 6  months

                    precision    recall  f1-score   support

        -1.0            0.44      0.02       0.04      1732
         1.0            0.56      0.98      0.71      2211

    accuracy                           0.56      3943
   macro avg       0.50      0.50      0.38      3943
weighted avg       0.51      0.56      0.42      3943

# Training data with an offset of 12 months

                     precision  recall  f1-score   support

     -1.0                0.00      0.00      0.00      1497
      1.0                0.56      1.00      0.72      1931

    accuracy                       0.56      3428
   macro avg       0.28      0.50      0.36      3428
weighted avg       0.32      0.56      0.41      3428

# Training data with an offset of 36 months

                      precision    recall  f1-score   support

        -1.0              0.00      0.00      0.00       772
         1.0              0.55      1.00      0.71       948

    accuracy                                      0.55      1720
    macro avg       0.28      0.50      0.36      1720
weighted avg       0.30      0.55      0.39      1720



### Step 2: 

## What impact resulted from increasing or decreasing either or both of the SMA windows?

The precision of the -1 class  increases  while the longer term window is greater  but the 1 class remains consistant. The recall moves to 0.0 for the ?1 class and  the 1 class is at or near 1.0. Based on the higher recall, it seems that the model (based on the training data) is better at predicting the 1 class than the ?1 class.
            
short_window = 4
long_window = 100

      
             precision    recall  f1-score   support

        -1.0       0.43      0.04      0.07      1804
         1.0       0.56      0.96      0.71      2288

    accuracy                           0.55      4092
   macro avg       0.49      0.50      0.39      4092
weighted avg       0.50      0.55      0.43      4092

           LR -  precision    recall  f1-score   support

        -1.0       0.44      0.33      0.38      1804
         1.0       0.56      0.66      0.61      2288

    accuracy                           0.52      4092
   macro avg       0.50      0.50      0.49      4092
weighted avg       0.51      0.52      0.51      4092

short_window = 50
long_window = 200
             
 precision    recall  f1-score   support

        -1.0       0.62      0.00      0.01      1667
         1.0       0.56      1.00      0.72      2138

    accuracy                           0.56      3805
   macro avg       0.59      0.50      0.36      3805
weighted avg       0.59      0.56      0.41      3805

          LR    precision    recall  f1-score   support

        -1.0       0.45      0.20      0.28      1740
         1.0       0.56      0.81      0.67      2227

    accuracy                           0.54      3967
   macro avg       0.51      0.51      0.47      3967
weighted avg       0.52      0.54      0.50      3967

short_window = 10
long_window = 20
             
           precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00      1828
         1.0       0.56      1.00      0.72      2324

    accuracy                           0.56      4152
   macro avg       0.28      0.50      0.36      4152
weighted avg       0.31      0.56      0.40      4152

       LR       precision    recall  f1-score   support

        -1.0       0.44      0.14      0.21      1828
         1.0       0.56      0.86      0.68      2324

    accuracy                           0.54      4152
   macro avg       0.50      0.50      0.45      4152
weighted avg       0.51      0.54      0.47      4152

  
short_window = 5
long_window = 20
          

 precision    recall  f1-score   support

        -1.0       0.00      0.00      0.00      1834
         1.0       0.56      1.00      0.72      2328

    accuracy                           0.56      4162
   macro avg       0.28      0.50      0.36      4162
weighted avg       0.31      0.56      0.40      4162

LR             precision    recall  f1-score   support

        -1.0       0.43      0.15      0.22      1828
         1.0       0.56      0.85      0.67      2324

    accuracy                           0.54      4152
   macro avg       0.50      0.50      0.45      4152
weighted avg       0.50      0.54      0.47      4152


### Step 3: 

The chart "Actual_Returns_vs_Strategy_Returns_SMA50_SMA200" shows a consistenly better performance in theStrategy Returns thn the actual returns while also sdaying in alignment with the Actual Returns. Therefore shjowing a truer predicted returns to the actuals.
