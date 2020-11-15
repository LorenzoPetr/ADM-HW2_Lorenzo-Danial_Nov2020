# ADM-HW2_Lorenzo-Danial_Nov2020
Git Repository containing the JupyterLab notebook for ADM's HW2

This repository contains the solution for HW2 provided by the two members of Group #22: **Lorenzo Petroni** and **Danial Abri**.

This README file was written specifically to provide a key to the contents of the notebook and the results obtained.

Although the code provided is complete, for what concerns the exercises proposed in the assignment, we have encountered several difficulties in testing the entire code with the complete dataset.
We have tried to set up instances on both AWS-S3 and Google Colab, in both cases without success.
The reasons were many: sometimes due to lack of RAM space on the virtual machine or, more frequently, for the time required for execution which always caused a kernel breakdown after hours of runtime.
To try to overcome this problem, we tried to load a different dataset for each assignment, loading each time only the fields we needed to solve the exercise.
However, even in this case, the solution was not sufficient to allow normal execution of all parts of the code.
We found an example of this situation in the code in **Exercise 1.3**, where we needed all records with event_type = "view" (the vast majority of total records).

So we decided to go like this: for both the October and November datasets we only uploaded 500000 records, so the aggregate dataset has one million records.
This allowed us to run the code locally without too many problems or slowdowns. 
However, many of the results shown in the notebook will be strongly influenced by this initial choice.

An obvious example can be found in the solution shown for **Exercise 5.1** in which it is possible to view the average number of views only for Mondays and Tuesdays.
The reason for this is that the complete dataset is sorted according to the **event_time** field. 
Therefore, by truncating the two datasets both to just 500000 records, information on the last days of the week is lost.
