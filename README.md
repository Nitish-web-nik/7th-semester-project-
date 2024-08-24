# 🕵️‍♂️ DETECTION OF PHISHING WEBSITES USING MACHINE LEARNING 🧠💻

## 🎯 Objective

Phishing websites are like the online equivalent of a wolf in sheep's clothing, trying to trick you into giving away your precious secrets—like your username and password—by pretending to be something they're not. It's a classic con game, but in the digital world! 🎭

The mission? To train some seriously smart machine learning models and deep neural networks to spot these shady sites before they can steal your info. We gathered a bunch of both phishing and legitimate URLs to create a dataset, extracted all the juicy features, and then put our models to the test. May the best model win! 🏆

## 🗂️ Data Collection

**Phishing URL Dataset** 🐟
We went phishing (but not the fun kind) and snagged ourselves a set of URLs from the fine folks at **PhishTank**. They generously provide a regularly updated list of phishing URLs in all sorts of formats. We grabbed 5,000 random phishing URLs from this treasure trove to train our machine learning models. You can check out PhishTank's catch of the day [here](https://www.phishtank.com/developer_info.php).

**Legitimate URL Dataset** 🛡️
Of course, we needed some good, upstanding URLs to balance things out. For that, we turned to the University of New Brunswick's dataset, which is like a URL farm with all sorts of benign, spammy, phishy, malware-laden, and defacement-prone links. We cherry-picked 5,000 benign URLs to teach our models how to tell friend from foe. More on that dataset [here](https://www.unb.ca/cic/datasets/url-2016.html).

Both datasets are safely stashed in the [DataSets folder](https://github.com/goodydeves/PhishBuster/tree/master/ML%20work/DataSets) of this repository, ready for action.

## 🔍 Feature Extraction

To give our models a fighting chance, we armed them with 17 powerful features extracted from the URL data. Think of these features as the clues our machine detectives use to sniff out the bad guys:

1. **Address Bar Based Features** 🛑
   - 9 features that focus on what’s happening in the URL’s address bar. Is that a suspiciously long domain name, or maybe a shady-looking subdomain? We’ve got it covered.

2. **Domain Based Features** 🌐
   - 4 features that dig into the domain itself. Is it registered to a sketchy IP address? Maybe it’s a baby domain, just a few days old. 🚼

3. **HTML & Javascript Based Features** 💻
   - 4 features that peek under the hood, checking the HTML and Javascript for anything that looks like it’s up to no good. 🚨

All these features combined give our models the info they need to make the right call. You can dive deeper into the feature set over at the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Phishing+Websites).

## 🧠 Models & Training

Before we let our models loose on the data, we split it into an 80/20 ratio—because life is all about balance, right? 🧘‍♂️ That’s 8,000 samples for training and 2,000 for testing. Since this is a supervised machine learning task, we’re classifying URLs as either phishing (1) or legitimate (0). The models we trained include:

- **Decision Tree** 🌳
- **Random Forest** 🌲
- **Multilayer Perceptrons** 🤹‍♂️
- **XGBoost** 🚀
- **Autoencoder Neural Network** 🤖
- **Support Vector Machines** 🏇

After the training montage (cue the Rocky music 🥊), we evaluated each model’s performance. Spoiler alert: **XGBoost** took home the gold for highest accuracy! 🥇 We even integrated the best features into a web application using Django to efficiently catch phishing URLs in the wild.

## 🛠️ Tools Used

Our arsenal of tools included:

- **Jupyter Notebook** 📓
- **PyCharm** 🛠️
- **Postman** 🚚
- **Chrome Browser** 🌐

## 🎥 Presentations & More

Here’s where you can find all the extras:

- **Project Summary Video** 🎬: "Project Summary.mp4"
- **Slide Presentation** 📊: "presentation slides.ppt"
- **Write-up Documentation** 📝: "Chapter 1-5 DETECTING PHISHING WEBSITES USING MACHINE LEARNING.pdf"

## 🌐 Web Application: PhishBuster

To take things to the next level, I created a web application named "PhishBuster" to help users validate website links. You can find it in the "Project_Webapp.7z" folder. Now, everyone can fend off phishing attacks like a pro! 🦸‍♂️🦸‍♀️

## 💻 ML Work

The **ML Work** folder contains:

- **Dataset** 📂
- **Jupyter Notebook** of the project:
  - **Phishing Website Detection Training & Testing Models on Datasets.ipynb**
  - **URL Feature Extraction from Datasets.ipynb**

## 🚀 Next Steps

What’s next? Well, the sky's the limit! 🌟 This project could easily be expanded into a browser extension for Chrome, Brave, Opera Mini, and more. Imagine a world where you could instantly spot phishing URLs just by browsing—no more worrying about that suspicious email from "BankofYourMoney.com"! 😜

---

Happy Phish Hunting! 🎣🔍
