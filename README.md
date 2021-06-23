# Flight Fare Prediction: 

## Edit
This is a extension of the project https://github.com/Mandal-21/Flight-Price-Prediction.git where I have pushed a new fligh_rf.pkl (101MB) file to the main repository using git-lfs (Large File Storage) to give a more accurate predicion of plane fares. I have created a guide detailing the steps of this process with regards to upload in github and deployment in heroku.
This could not be a contribution to the original project as github does not allow git-lfs uploads to forked repositories where the main repository does not contain a git-lfs uploaded file.

## Table of Content
  * [Demo](#demo)
  * [Overview](#overview)
  * [Installation](#installation)
  * [Deployement on Heroku](#deployement-on-heroku)
  * [Directory Tree](#directory-tree)
  * [Bug / Feature Request](#bug---feature-request)
  * [Future scope of project](#future-scope)
  * [Git lfs upload of tuned hyper-parameter model](#git-lfs)


## Demo
Link: [https://flight-price-prediction-api.herokuapp.com/](https://flight-price-prediction-api.herokuapp.com/)

[![](https://i.imgur.com/R1g2wvC.png)](https://flight-price-prediction-api.herokuapp.com/)

[![](https://i.imgur.com/p0aeL6c.png)](https://flight-price-prediction-api.herokuapp.com/)

## Overview
This is a Flask web app which predicts fare of Flight ticket.

## Installation
The Code is written in Python 3.6.10. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:
```bash
pip install -r requirements.txt
```

## Deployement on Heroku
Login or signup in order to create virtual app. You can either connect your github profile or download ctl to manually deploy this project.

[![](https://i.imgur.com/dKmlpqX.png)](https://heroku.com)

Our next step would be to follow the instruction given on [Heroku Documentation](https://devcenter.heroku.com/articles/getting-started-with-python) to deploy a web app.

## Directory Tree 
```
├── static 
│   ├── css
├── template
│   ├── home.html
├── Procfile
├── README.md
├── app.py
├── flight_price.ipynb
├── flight_rf.pkl
├── requirements.txt
```

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

[<img target="_blank" src="https://flask.palletsprojects.com/en/1.1.x/_images/flask-logo.png" width=170>](https://flask.palletsprojects.com/en/1.1.x/) [<img target="_blank" src="https://number1.co.za/wp-content/uploads/2017/10/gunicorn_logo-300x85.png" width=280>](https://gunicorn.org) [<img target="_blank" src="https://scikit-learn.org/stable/_static/scikit-learn-logo-small.png" width=200>](https://scikit-learn.org/stable/) 


## Bug / Feature Request

If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an [issue](https://github.com/Mandal-21/Flight-Price-Prediction/issues) here by including your search query and the expected result

## Future Scope

* Use multiple Algorithms
* Optimize Flask app.py
* Front-End 

## Git LFS

GIT-LFS is required to push the tuned hyper-parameter model to the master repo as github does not allow upload of files larger than 100MB.
For a step by step guide on how to install and push your large files to github click [here](https://git-lfs.github.com/).
 
 For deployment in Heroku a buildpack is needed for git-lfs files. The package with instructions can be found [here](https://elements.heroku.com/buildpacks/teawkung/heroku-buildpack-git-lfs), or this can also be done manually in Heroku by going to your app settings > Buildpacks and adding the clone of the buildpack git repository.
 There is also a requirement to add [convig variables](https://stackoverflow.com/questions/62532673/how-to-deploy-git-lfs-on-heroku) which can be added manually by going to app > settings > convig var. You first need to set the first key to 'BL_BUILDPACK_GIT_LFS_REPO' and value to the clone URL of your repository in which the lfs file is situated.For the next config var, an SSH key should be generated and added as the value to the key 'BL_BUILDPACK_GIT_LFS_SSH_PRIVATE_KEY'. Here is some advice on [generating SSH keys](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
 



