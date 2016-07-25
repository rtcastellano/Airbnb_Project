This repository is related to a Kaggle competition hosted by Airbnb https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings
The goal of this competition is to predict the country in which a new user will make his/her first booking. You are allowed
to submit up to 5 suggestions and are ranked based on how relevant these suggestions are. For more details, see the competition
rules

All work in this repository was done in collaboration with Yannick Kimmel, Zi Jin, and Michael Winfield.

My_Airbnb_Presentation.pdf is the presentation I will give and contains an overview of our strategy and model.

/EDA contains code for exploratory data analysis
/EDA_Graphs contains the resulting graphs

/ShinyMap/AirbnbBookings contains the code for a shiny app that describes the problem, gives information about the possible
destination countries, and displays EDA regarding the competition
A working version of this app can be accessed at https://rtcastellano.shinyapps.io/AirbnbBooking/

/Scripts contains the scripts for our models (which I will describe below).
/Workflow.png gives a schematic for out model:
  We used user information to predict time-lag variables (using rf and gbm). We then put these predictiong into an adaboost and
  xgboost model to predict country destination.
  
  We also ran an xgboost model directly on the user information
  
/Scripts
  /DataPreprocessing.ipynb contains preprocessing code
  
  /FE&Stacking_GBM.R contains stacking via gbm
  
  /RandomForest_Stacking.ipynb contains stacking via ranfom forests

  /AdaBoost_CodeandResults.ipynb contains the code for AdaBoost on stacked data
  
  /XGBoost_stacked.ipynb contains the code for XGBoost on stacked data
  
  /XGBoost_Unstacked.ipynb contains the code for XGBoost on the unstacked data
  
  

