Spotted a mistake, dead link, or have suggestions for improvements? Give us a shout using the [links below](#contact).

**Navigation**

* [Introduction](#introduction)
  * [Important First Steps](#important-first-steps)
  * [Welcome to the Hackathon](#welcome-to-the-hackathon)
  * [Event Timeline](#event-timeline)
* [Competitions Details](#competition-details)
  * [Machine Learning Competition](machine-learning-competition)
  * [Data Story-Telling Competition](data-story-telling-competition)
  * [Prizes](#prizes-and-sponsors)
* [Hackathon Parters](#hackathon-partners)
  * [Heart of England](#heart-of-england)
  * [SIG Susquehanna](#sig-susquehanna)
* [Help and Information](#help-and-information)
  * [FAQs](#faqs)
  * [Getting Help](#getting-help)
  * [Contact](#contact)
  * [Socials](#socials)

## Introduction

### Important First Steps

There's a lot of information on this page but here are the most important steps to take to get involved in the hackathon:

1. Join the [Microsoft Teams team](https://teams.microsoft.com/l/team/19%3a29e7091294a54889b597e0b482357a03%40thread.tacv2/conversations?groupId=65592f3f-20ad-41a8-b0a9-cece40e28023&tenantId=09bacfbd-47ef-4465-9265-3546f2eaf6bc) for the hackathon and turn on notifications in all channels to avoid missing out on any important updates
2. If you've not already, checkout the [kick-off talk](https://www.youtube.com/watch?v=RgifF8rLbX4) on YouTube
3. Click 'Going' on the hackathon's [Facebook event](https://www.facebook.com/events/824273791735565/) to be notified when workshops are arranged
4. If you wish to take part in the machine learning competition, you will likely want to form a team. Checkout the 'Networking' channel in teams for discussions/networking sessions on forming teams. Once you have a team, fill in the form [here](https://forms.microsoft.com/Pages/ResponsePage.aspx?id=vc-6Ce9HZUSSZTVG8ur2vOEbfIgZakBLnZEi9heYVBtUNVNVMEtHN0dMWlA1VFZBVFZQT0k1UVgzVy4u), and we will get in touch soon after with your login details for the submission portal.

All other relevant details should be available on this page, but if you have any questions, feel free to reach out to us using the contact links [below](#contact). Happy hacking!

### Welcome to the Hackathon

The Helping Hack Charity Hackathon is designed to be an inclusive event for anyone to attend, with the aim of giving back to the community using our data science skills.
As such we have teamed up with the local Midlands-based charity, Heart of England, as well as working with our friends at Warwick Statistics Society to set up this exciting virtual event. This two-day hackathon involves talks, workshops and some thrilling competitions with great prizes on offer!

The hackathon consists of two main competitions: a two-day machine learning competition and a three-week data story-telling competition. Full details on these can be found [below](#competiton-details).

### Event Timeline

A rough agenda for the hackathon is as follows.

|      Date     |   Time   |                 Item                |
|:-------------:|:--------:|:-----------------------------------:|
| 13th November | 6-6.30pm |         Live talk on YouTube        |
| 13th November | 6.30-7pm |   Networking/team-forming session   |
| 13th November |    7pm   |  Instructions and datasets released |
| 14th November |   4-5pm  |      Check-in session on Teams      |
| 15th November |    7pm   |  Machine Learning competition ends  |
|  4th December |    7pm   | Data story-telling competition ends |

Competition winners will be announced and prizes given out soon after the hackathon ends.

We will also be hosting numerous workshops to support less experienced data scientists with the hackathon. This list will be updated as we confirm events, at which point they will also be posted in the hackathon's [Facebook event](https://www.facebook.com/events/824273791735565/), so make sure to click 'Going' there.

|      Date     |    Time    |            Agenda            |
|:-------------:|:----------:|:----------------------------:|
| 14th November | 10-10.45am |    Machine Learning with R   |
| 14th November | 11-11.45am | Machine Learning with Python |

#### Workshop Recordings/Resources

- Machine Learning with R
  - Video (Coming soon)
  - [HTML Notebook](http://warwickdatascience.github.io/helping-hack-heart-of-england/notebooks/tutorial.nb.html)
  - [Raw Notebook](https://raw.githubusercontent.com/warwickdatascience/helping-hack-heart-of-england/main/notebooks/tutorial.Rmd) (Open in RStudio Cloud)
- Machine Learning with Python
  - Video (Coming soon)
  - [Colab Notebook](https://colab.research.google.com/github/warwickdatascience/helping-hack-heart-of-england/blob/main/notebooks/tutorial.ipynb)

## Competition Details

### Machine Learning Competition

#### Brief

The objective of this competition is to understand and predict how local authority spending will impact indices of deprivation over time. To investigate this problem, WDSS has collated and cleaned a selection of relevant datesets, described below. 

Your task is to predict the values that we have deliberately removed from the dataset using machine learning techniques.

#### Resources

Although many other relevant datasets are available on the web, submissions for this competition are restricted to only use the datasets provided on this page, to maintain a focus on machine learning enginuity.

The most important dataset is [imd.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/imd.csv). This gives indices of multiple deprivation for multiple local authorities districts (identified by their ONS code `lad_code` and name `lad_name`) in both 2015 and 2019. 20% of 2019 indices have been removed. It is your job to predict these using machine learning.

To aid in this task, you are provided with the dataset [ref.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/imd.csv) which contains revenue expenditure and financing data for these same local authority districts over the years 2016 to 2019. 

Each expense (`expense`) is assigned a expense category (`category`) and has an associated expenditure for each year/local authority (`expenditure`) which is measured in thousands of pounds. Note, this can be negative if a profit was made (for example of a local authority car park brings in more profit than its upkeep cost).

In fact, this datasets contains expenses for more than just local authorities. The `class` column breaks down the types of local authority district as so:

```
LONDON BOROUGHS		L
METROPOLITAN DISTRICTS		MD
UNITARY AUTHORITIES		UA
SHIRE COUNTIES		        SC
SHIRE DISTRICTS		SD
OTHER AUTHORITIES		O
```

Metropolitan and other authorities (e.g. police force areas) do not appear in the `imd.csv` dataset but may provide useful information. For example, police/fire spending is rarely performed at a local authority level and so may need to be taken from these larger collectives.

Local authority lookup tables are provided for this purpose:

- Combined Authorities: [lad_ca_lut.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/lad_ca_lut.csv)
- Counties: [lad_cty_lut.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/lad_cty_lut.csv)
- Fire and Rescue: [lad_far_lut.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/lad_far_lut.csv)
- Police Force Areas: [lad_pfa_lut.csv](https://warwickdatascience.github.io/helping-hack-heart-of-england/resources/lad_pfa_lut.csv)

`ref.csv` also contains information on national parks and waste facilities but lookup tables for these are hard to come by. Manual lookups or regex matching would be valid workarounds to this problem if one felt it was necessary.

#### Submission

To submit, you will need to have created a team using [this form](https://forms.microsoft.com/Pages/ResponsePage.aspx?id=vc-6Ce9HZUSSZTVG8ur2vOEbfIgZakBLnZEi9heYVBtUNVNVMEtHN0dMWlA1VFZBVFZQT0k1UVgzVy4u). Once this is filled out, you will soon recieve an email giving you login details to our [submission portal](https://cloud.wdss.io/).

You can use this portal to submit (as often as once per hour) a submission CSV file along with a Jupyter notebook that can be used to generate the CSV. 

The submitted CSV should be a copy of `imd.csv` but with missing values replaced with your predictions.

The competition will run from **7pm on Friday the 13th November** to **7pm on Sunday the 5th December**.

#### Judging

For each submission, the RMSE score is computed using the testing data (that is, rows that previously had missing values). As a rule of thumb, this will treat a few large errors worse than several small errors.

This submission with the best RMSE for each team will be displayed on the leaderboard.

**These scores alone will not be used to determine the final winner.**

Instead, a bootstrapped RMSE will be computed for each submission. This consists of randomly resampling the test set and computing the RMSE for this sample, averaging over multiple interations. The purpose of this technique is to avoid model overfitting through repeated submissions. 

You can improve your confidence that this bootstrapping procedure what not decrease your score by implementing cross-validation when building your model.

As a final point, we are well aware the correct answers for this task are available on the web. That said, we will be thoroughly checking the corresponding notebook for the winning submission to make sure that no data external to what we provided is used.

#### Advice

A few words of advice from the competition author:
- The predictor data supplied in this competition is rich and powerful, but vastly overshadows the response data in size. For that reason, [regularisation](https://towardsdatascience.com/regularization-in-machine-learning-76441ddcf99a) is the key to success
- Multi-level modelling approaches are a good way to combine the entirety of the data together
- Although you can't use other data sources than those provided by us, research into the metrics of use, in particular the [revenue expense and financing data](https://www.gov.uk/government/collections/local-authority-revenue-expenditure-and-financing), is a worthy investment of time
- Start simple and build up; you may be suprised how well a well-crafted linear model can perform.

We will also be running two workshops on Saturday morning in both R and Python, walking through how to build a baseline model that can be improved upon by incorparating the full datasets, using feature engineering, and employing more complex models. You can find details of these events [above](#event-timeline).

Two models for comparison have been provided by WDSS. These are:
- A null model: predicting no change in IMD from 2015 to 2019 for each LAD
- A baseline model: the simple linear regression model described in the introductory workshop

Ideally, your model should outperform both of these.

### Data Story-Telling Competition

#### Brief

The three areas of interest proposed by Heart of England are:

1. How has COVID-19 changed the need for funding?
2. In what ways does discrimination impact the success of BAME-led organisations?
3. What is the impact of poor environmental standards on life expectancy and quality of living?

Your task is to pick one of the questions ([or more if you wish](#faqs)) and create a visualisation, blog post, report, graphic, etc. that offers insight into these questions using data. These questions are deliberately broad so feel free to be creative in how you tackle the problems.

#### Resources

The goal of this competition is for participants to perform their own research and find relevant data resources. That said, here are a few useful places to look for datasets:

- [Office for National Statistics](https://www.ons.gov.uk/)
- [Kaggle Datasets](https://www.kaggle.com/datasets)
- [UK Goverment Data](https://data.gov.uk/)
- [Data World (UK)](https://data.world/datasets/uk)

#### Submission

Submissions should be sent to [hackathon@wdss.io](mailto:hackathon@wdss.io).

The competition will run from **7pm on Friday the 13th November** to **7pm on Friday the 4th December**. No preference will be given to early entrants.

#### Judging

Submissions will be judged by our partner charity [Heart of England](#heart-of-england). It is therefore worth understanding their objectives to maximise your chances of impressing/inspiring them with your work.

They will declare a winning submission for each of the three questions above, as well as a bonus wildcard winner.

## Prizes

The members of the winning team for the machine learning competition will each be supplied with a pair of wireless headphones.

For the data-storytelling competition, a SIG goodie bag will be awarded to the winner for each category, as judged by [Heart of England](#heart-of-england), with one additional goodie bag being offered to a notable runner-up.

## Hackathon Parters

### Heart of England

We are working with Heart of England, a charity that raises money to fund and develop local community activity across the West Midlands and Warwickshire. Since 1995, they have distributed over £16 million locally, benefiting an estimated 2 million people. 

In 2017/18 they awarded over £2.5 million to support communities across the West Midlands to thrive. Similarly, their endowment fund has also grown to £9.4 million, providing a continued legacy for communities.

Their amazing work helping communities inspired us to work with them on this hackathon. You can read more about the projects they do [here](https://www.heartofenglandcf.co.uk/).

### SIG Susquehanna

This event is sponsored by SIG Susquehanna, a global quantitative trading firm founded with an entrepreneurial mindset and a rigorous analytical approach to decision making.

SIG’s Quantitative Trader Programme, and Trading Internship, is widely recognized as the industry’s leading trading education programme. All of SIG’s education is taught in house by Senior Traders and combines hands-on practical experience, quantitative project work and game theory education. You don’t need to have any financial experience or knowledge to be a trader in SIG, they’ll teach you everything you need to know. Applications for the 2021 QT Programme and internship are open now. Follow [this link](https://www.sig.com/campus-programmes/trading/) to learn more.

## Help and Information

### FAQs

#### How many team members am I allowed?

The data story-telling competition is strictly for individual participation whilst the machine learning competition has has a maximum team size of four. 

If you don't have a team, but would like to be part of one, either join a networking session or leave a message in the 'Networking' channel of the hackathon [team](https://teams.microsoft.com/l/team/19%3a29e7091294a54889b597e0b482357a03%40thread.tacv2/conversations?groupId=65592f3f-20ad-41a8-b0a9-cece40e28023&tenantId=09bacfbd-47ef-4465-9265-3546f2eaf6bc).

#### Can I make multiple submissions to the data story-telling competition?

Each individual is allowed to make one submission for each of the questions of interest. In such a case, it would be possible that this participant would win all three category prizes.

#### I've improved my data story-telling submission since last submitting. Can I resubmit?

No problem. Simply email [hackathon@wdss.io](mailto:hackathon@wdss.io) and explain the situation.

### Getting Help

Help will be provided throughout the hackathon in a number of ways:
- Most help can be found by messaging 'Get Help' channel on [Teams](https://teams.microsoft.com/l/team/19%3a29e7091294a54889b597e0b482357a03%40thread.tacv2/conversations?groupId=65592f3f-20ad-41a8-b0a9-cece40e28023&tenantId=09bacfbd-47ef-4465-9265-3546f2eaf6bc)
- We will also hold some live Q&A sessions

### Contact

This hackathon was written and is primarily managed by Tim Hargreaves. He can be contacted most easily via Microsoft Teams but is also highly responsive on [LinkedIn](https://www.linkedin.com/in/tim-hargreaves/).

### Socials

#### Warwick Data Science Society

- [Facebook](https://link.wdss.io/facebook)
- [Linkedin](https://link.wdss.io/linkedin)
- [Instagram](https://link.wdss.io/instagram)
- [YouTube](https://link.wdss.io/youtube)

#### Warwick Statistics Society

- [Facebook](https://www.facebook.com/WarwickStatsSociety)
- [Linkedin](https://www.linkedin.com/company/warwickstatisticssociety/)

