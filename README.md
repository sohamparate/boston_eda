

## First Look at the data
- `chas` is binary and `rad` has a limited number of values.
- Is it possible to determine `medv` using chas alone? No. It's nowhere close
- Is there a relationship between `rad` and `medv`? Not really.
- Is there any column that single handedly identifies?
- A high value of `lstat` means a lower value of `medv`


## HeatMap
Note: I have normalised the data(except for chas column) before calculating this heatmap in order to help combine two columns.


<img width="609" alt="image" src="https://github.com/user-attachments/assets/ec64cb3f-45ac-4b09-bbbb-9a561beac284" />


In the above heatmap, there are some columns that show the exact same behaviour against medv, let’s combine them…


<img width="608" alt="image" src="https://github.com/user-attachments/assets/08440026-70be-4562-a0cc-2643e7a8db0b" />


I have used MinMax normalization technique to combine the two columns. I found that the simplest to get the job done.

We can combine it a step further…

<img width="533" alt="image" src="https://github.com/user-attachments/assets/1a705b4e-b76a-4343-b5c3-ece7e891c961" />


resulting columns are `dis_b_zn_rm` & `age_ptratio_lstat_tax_rad_indus_nox_crim` & `medv`


## Conclusion
In this simplified heatmap, we can conclude that:
- `chas` is useless.
- If `age_ptratio_lstat_tax_rad_indus_nox_crim` is low, `medv` is high.
- If `dis_b_zn_rm` is high, `age_ptratio_lstat_tax_rad_indus_nox_crim` is low.
- As a result,
- If `dis_b_zn_rm` is high, `medv` is high.


