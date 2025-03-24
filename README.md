# Codeforces User Analysis based on code project

## Structure of Project

**data**
- **users_codes.csv:**
  - `id` *(Int)* – task submission ID on Codeforces  
  - `user` *(String)* – handle of the user who submitted the code  
  - `rating` *(Int)* – user’s rating at the time of submission  
  - `date` *(Datetime)* – date of the task submission  
  - `code` *(String)* – submitted code

**preparing**
- **data_collecting.ipynb**

  This file uses the public Codeforces API to fully extract submissions and code of all active users (those who have participated in at least one round in the last 6 months)

- **tasks_information.csv:**
  - `id` *(Int)* – unique problem ID on Codeforces  
  - <code>topic<sub>i</sub></code> *(Boolean)* – one-hot encoded columns representing the presence of each topic in the problem (e.g., `{graphs}`, `{dp}`, etc)

**models**
  - **codes_clusteting.pkl**
    
    This file contains trained model that clustering code using its content as input
    
  - **users_clustering.pkl**
    
    This file contains trained model that clustering users based on their rating and a set of problematic topics
  
**training**
  - **codes_clusteting.ipynb**
    
    This file implements training of a model to clustering code based on identified topics and saving the model to `codes_classification.pkl`
  
  - **users_clustering.ipynb**
    
    This file implements training for clustering users and saving the model to `users_clusterization.pkl`

### The project is actively under development. README and files will be updated regularly
