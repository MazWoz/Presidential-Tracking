# Presidential Approval Tracker

### This repository contains a model that tracks and predicts presidential approval ratings based on various policy areas. The model uses polling data from various pollsters and incorporates pollster ratings from Nate Silver (https://www.natesilver.net/).

### The python is fairly straight forward and uses a Gaussian Process model from sklearn to provide a smoothed history and predictive trajectory (30 days).
### The model also includes an exponential decay with a half-life of 14 days for recency bias, and weights Likely Voter (LV) samples as the highest and Adult (A) samples as the lowest with Registered Voters (RV) as the median polling sample weight.
### Additionally, I've included a fairly robust method for adjusting pollster bias, assuming a 50/50 split for pollster bias -- meaning if a pollster is +2 (D+2) I assume that the bias is half approval, half disapproval versus 100% approval and 100% disapproval.
### The output is a series of interactive charts that can be found in the analysis/files folder. These charts are also pushed to a GitHub Pages site for easy viewing: https://mazwoz.github.io/Presidential-Tracking/
### I pull my polling data directly from NateSilver on a regular basis.

#### If you are using this code, please pull directly from Nate's site for the recent polling data and name the files accordingly:
1. current.csv -- Overall Presidential Approval
2. economy.csv -- Economic Policy Approval
3. trade.csv -- Trade Policy Approval
4. immigration.csv -- Imigration Policy Approval
5. inflation.csv -- Inflation Policy Approval

#### Please note that I have also included a workflow that will automatically convert the Jupyter Notebook to an HTML file and push it to the main branch for easy viewing. This workflow runs every time I push an update.