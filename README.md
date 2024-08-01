# Underground Music Discovery
The architecture of a music discovery feature that can be implemented into social media platforms (TikTok, Instagram, Snapchat, etc.) 

# Origin and Purpose
Born out of participation in the TikTok TechJam 24, this project is meant to use the data generated and collected in user profiles of a social media platform and leverage machine learning to generate recommendations of 'underground' songs for the user. And example of such data could be the different metrics that are used to measure how users interact with songs attached to the content of these platforms. For this project, due to lack of access to the APIs of such platforms, we have used a Spotify playlist as a proxy for this dataset. The dataset used to recommend songs was created through a combination the use of a web scraper and Kaggle. we defined 'underground' as artists with monthly listeners between 100,000 and 1,000,000 at the time the data was collected. The final product combined the engine with a demo of the frontend.

# My Role
I was chiefly responsible for the creation of the recommendation engine, and after considering well-known options such as a Boltzmann machine for a neural network-driven system, I settled on a TF-IDF based system. The engine was written entirely Python on JupyterLab, and leveraged Scikit Learn, Pandas, Numpy, and Spotipy libraries. 

# Challenges
The most time was spent processing the data and manipulating it into a form that could generate the best recommendations. The engine was reliant on nearly a dozen parameters collected from the Spotify API, but for the use of TF-IDF, the parameters were expanded vastly to 15000+. This was done by creating a feature set of the many different genres songs fall under, and applying the TF-IDF vectorizer on that feature set to give weight to certain matches in genre between the recommended songs and the ones in the user's profile. Finding ways to extrapolate this from raw data was challenging. 
