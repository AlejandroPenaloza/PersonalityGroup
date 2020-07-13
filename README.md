# PersonalityGroup
Based on the Big Five Personality Traits (FFM: Five-Factor Model), a Personality Group will be output for each case. M

Dataset obtained from Kaggle: https://www.kaggle.com/tunguz/big-five-personality-test?

This program is meant to set for each given case (which represents a person psychological test answers) a Personality Group.
FFM is a suggested taxonomy, or grouping, for personality traits, developed from the 1980s onwards. When factor analysis (a statistical technique) is applied to personality survey data, some words used to describe aspects of personality are often applied to the same person.
Whole explanation available in https://en.wikipedia.org/wiki/Big_Five_personality_traits

![400px-Wiki-grafik_peats-de_big_five_ENG](https://user-images.githubusercontent.com/56207845/86517328-ba606600-bded-11ea-935d-af4e9b666b0b.png)

### Dataset description is the following:
    
    This data was collected (2016-2018) through an interactive on-line personality test.
    The personality test was constructed with the "Big-Five Factor Markers" from the IPIP. https://ipip.ori.org/newBigFive5broadKey.htm
    Participants were informed that their responses would be recorded and used for research at the beginning of the test, and asked to confirm their consent at the end of the       test.

    The following items were presented on one page and each was rated on a five point scale using radio buttons. The order on page was was EXT1, AGR1, CSN1, EST1, OPN1, EXT2,       etc.
    The scale was labeled 1=Disagree, 3=Neutral, 5=Agree

    EXT1	I am the life of the party.
    EXT2	I don't talk a lot.
    EXT3	I feel comfortable around people.
    EXT4	I keep in the background.
    EXT5	I start conversations.
    EXT6	I have little to say.
    EXT7	I talk to a lot of different people at parties.
    EXT8	I don't like to draw attention to myself.
    EXT9	I don't mind being the center of attention.
    EXT10	I am quiet around strangers.
    EST1	I get stressed out easily.
    EST2	I am relaxed most of the time.
    EST3	I worry about things.
    EST4	I seldom feel blue.
    EST5	I am easily disturbed.
    EST6	I get upset easily.
    EST7	I change my mood a lot.
    EST8	I have frequent mood swings.
    EST9	I get irritated easily.
    EST10	I often feel blue.
    AGR1	I feel little concern for others. 
    AGR2	I am interested in people.
    AGR3	I insult people.
    AGR4	I sympathize with others' feelings.
    AGR5	I am not interested in other people's problems.
    AGR6	I have a soft heart.
    AGR7	I am not really interested in others.
    AGR8	I take time out for others.
    AGR9	I feel others' emotions.
    AGR10	I make people feel at ease.
    CSN1	I am always prepared.
    CSN2	I leave my belongings around.
    CSN3	I pay attention to details.
    CSN4	I make a mess of things.
    CSN5	I get chores done right away.
    CSN6	I often forget to put things back in their proper place.
    CSN7	I like order.
    CSN8	I shirk my duties.
    CSN9	I follow a schedule.
    CSN10	I am exacting in my work.
    OPN1	I have a rich vocabulary.
    OPN2	I have difficulty understanding abstract ideas.
    OPN3	I have a vivid imagination.
    OPN4	I am not interested in abstract ideas.
    OPN5	I have excellent ideas.
    OPN6	I do not have a good imagination.
    OPN7	I am quick to understand things.
    OPN8	I use difficult words.
    OPN9	I spend time reflecting on things.
    OPN10	I am full of ideas.

    The time spent on each question is also recorded in milliseconds. These are the variables ending in _E. This was calculated by taking the time when the button for the question was clicked minus the time of the most recent other button click.

    dateload    The timestamp when the survey was started.
    screenw     The width the of user's screen in pixels
    screenh     The height of the user's screen in pixels
    introelapse The time in seconds spent on the landing / intro page
    testelapse  The time in seconds spent on the page with the survey questions
    endelapse   The time in seconds spent on the finalization page (where the user was asked to indicate if they has answered accurately and their answers could be stored and used for research. Again: this dataset only includes users who answered "Yes" to this question, users were free to answer no and could still view their results either way)
    IPC         The number of records from the user's IP address in the dataset. For max cleanliness, only use records where this value is 1. High values can be because of shared networks (e.g. entire universities) or multiple submissions
    country     The country, determined by technical information (NOT ASKED AS A QUESTION)
    lat_appx_lots_of_err    approximate latitude of user. determined by technical information, THIS IS NOT VERY ACCURATE. Read the article "How an internet mapping glitch turned a random Kansas farm into a digital hell" https://splinternews.com/how-an-internet-mapping-glitch-turned-a-random-kansas-f-1793856052 to learn about the perils of relying on this information
    long_appx_lots_of_err   approximate longitude of user

When importing the dataset, a random sample of 500000 cases was finally used for the data analysis.

The code presents the following sections:
            
    - PersonalityGroup
        - Importing and setting up the dataset
        - Exploratory Data Analysis
        - Data Preprocessing
        - K-Means Clustering
    
**After importing the dataset and implementing Data Wrangling, the program continues
with EDA (Exploratory Data Analysis) in order to go on with the Data Analysis focus and developing part.
With our dataset cleaned now will be separated into numerical and categorical data.**

**Numerical data scaled and categorical data encoded, the final formatted dataset is built
and ready to be used and fit on the ML model.**

**The Unsupervised Learning algorithm K-Means is used for this model, in order to find patterns
 and to define these clusters for the data be categorized.**

**Later on, the goal is stablishing the optimal number of clusters so the personality traits 
conform the best delimited classification for each case/row (person).**

**THEN, THESE CLUSTERS ARE SET FOR PEOPLE TO BE STORED ACCORDING
TO THEIR ANSWERS ON THE SURVEY (PROVIDED DATA), WHICH WERE BASED ON EACH
ONE FROM THE BIG FIVE PERSONALITY TRAITS.**
                                         
                                         **IT WAS DEFINED THESE GROUPS WHERE PEOPLE ARE IDENTIFIED BY THEIR PERSONALITY!**
