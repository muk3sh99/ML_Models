1. On the Amazon Fine Food Reviews dataset, there is a minor error in the calculation of class weights when using XGBoost with class balancing,
2. We are assigning less weight to the minority class (0) in this scenario.
3. The correct code will be scale_pos_weight = len(y_train[y_train == 1]) / len(y_train[y_train == 0])
4. Also ignore #scale positive weight comment
5. Correction2:
6. While calculating class distribution:
7. print("Class 0: ",int(test_distr[0])/test_len, "Class 1: ",int(test_distr[1])/test_len)
8. This is correct code.
