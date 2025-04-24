### IPL 2025 Toss and Match Winner Predictions

### About This Project
The "IPL Win Predictor" leverages logistic regression to provide insights into the probability of a team winning an IPL match. This model analyzes various match features, team performance, and player statistics to offer real-time predictions

### Technologies Used
This project leverages the following technologies:

1.Python
2.Logistic Regression
3.NumPy
4.pandas
5.Streamlit

 ### Match 1 : Kolkata Knight Riders vs Royal Challengers Bangalore
 **Date** : March 22 , 2025
 **Venue** : Eden Gardens , Kolkata
 
 ## Insight from  Historical data
- KKR has won 60% of the matches played against RCB in the last 5 years.
- RCB has won 40% of the matches played against KKR in the last 5 years.
- KKR has won toss 55% of the time in the last 5 years.
- RCB has won toss 45% of the time in the last 5 years.

###  Model Predictions

Toss Winner Prediction Accuracy: 55.71%
Match Winner Prediction Accuracy: 46.12%
 Toss Winner:* Royal Challengers Bangalore
 Match Winner:* Kolkata Knight Riders

###  Code Snippet (Final Decision)

python
def predict_winner(team1, team2,venue):
    if team1 not in team_encoder.classes_ or team2 not in team_encoder.classes_:
        raise ValueError(f"Unknown team: {team1} or {team2}")
    if venue not in venue_encoder.classes_:
        print(f"⚠️ Warning: Venue '{venue}' not in training data. Using fallback 'Wankhede Stadium'.")
        venue = 'Wankhede Stadium'
    t1 = team_encoder.transform([team1])[0]
    t2 = team_encoder.transform([team2])[0]
    v = venue_encoder.transform([venue])[0]
    d = decision_encoder.transform(['field'])[0]
    toss_encoded = toss_model.predict([[t1, t2, v]])[0]
    toss_winner = team_encoder.inverse_transform([toss_encoded])[0]
    winner_encoded = match_model.predict([[t1, t2, v, toss_encoded, d]])[0]
    match_winner = team_encoder.inverse_transform([winner_encoded])[0]
    return toss_winner, match_winner



----------------------------------------------------------------------------------------

## Match 2: Rajasthan Royals vs Sunrisers Hyderabad

*Date:* March 23, 2025\
*Venue:* Rajiv Gandhi International Stadium , Hyderabad

###  Insights from Historical Data

- Rajasthan Royals have won *48%* of tosses at this venue.
- Sunrisers Hyderabad have won *12* of the last *21* matches against RR.
- Teams batting second have a *62%* win rate at this venue.

###  Model Predictions
Toss Winner:* Sunrisers Hyderabad
Match Winner:* Sunrisers Hyderabad

-----------------------------------------------------------------------------------------------------------

## Match 3: Chennai Super Kings vs Mumbai Indians

*Date:* March 23, 2025\
*Venue:* MA Chidambaram Stadium, Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *57%* of tosses at Wankhede since 2010.
- MI holds a slight edge with 20 victories, while CSK has won 17 matches out of 37 encounters.
- MI Teams batting second have a *60%* win rate at this venue.

###  Model Predictions

Toss Winner:* Chennai Super Kings
Match Winner:* Mumbai Indians


--------------------------------------------------------------------------

## Match 4: Lucknow Super Giants vs Delhi Capitals

*Date:* March 24, 2025\
*Venue:* ACA-VDCA Cricket Stadium,Visakhapatnam

###  Insights from Historical Data

- LSG have won *54.54%* of matches since 2022-2024
- DC have won *44.44%* of matches since 2022-2024
- Teams batting first have a *55%* win rate at this venue.

###  Model Predictions

Toss Winner:* Lucknow Super Giants
Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------

## Match 5: Punjab Kings vs Gujarat Titans

*Date:* March 25, 2025\
*Venue:* Narendra Modi Stadium, Ahmedabad

###  Insights from Historical Data

- Punjab Kings have won *44%* of matches since 20022-2024
- Gujarat Titans have won *56* of matches since 2024
- Teams batting second have a *62%* win rate at this venue.

###  Model Predictions

Toss Winner:* Gujarat Titans
Match Winner:* Punjab Kings

-----------------------------------------------------------------------------------------------------------

## Match 6: Rajasthan Royals vs Kolkata Knight Riders

*Date:* March 26, 2025\
*Venue:* Barsapara Stadium, Guwahat

###  Insights from Historical Data

- Kolkata Knight Riders have won *55%* of against Rajasthan Royals .
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Kolkata Knight Riders
Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 7: Sunrisers Hyderabad vs Lucknow Super Giants

*Date:* March 27, 2025\
*Venue:* Rajiv Gandhi International Stadium , Hyderabad

###  Insights from Historical Data

- Sunrisers hyderabad has won Approximately 50​ of toss in matches
- Sunrisers Hyderabad has won Around 20% of matches last 5 matches
- Lucknow Super Giants have won *80* of matches in last 5 matches
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions
# Its only show the prediction done by analyzing the history of matches 
Toss Winner:* Sunrisers Hyderabad
Match Winner:* Lucknow Super Giants

-------------------------------------------------------------------------------------------

## Match 8: Royal Challengers Bangalore vs Chennai Super Kings

*Date:* March 28, 2025\
*Venue:* MA Chidambaram Stadium, Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *50%* of tosses since 2008-2024
- Chennai Super Kings have won *60%* of matches since 2008-2024
- Royal Challengers Bangalore has won approx. 45% of tosses since 2008-2024
- Royal Challenges bangalore has won *48%* of matche 
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Royal Challengers bangalore
Match Winner:* Chennai Super KIngs

-------------------------------------------------------------------------------------------

## Match 9: Gujarat Titans vs Mumbai Indians

*Date:* March 29, 2025\
*Venue:* Narendra Modi Stadium, Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *31%* of tosses at this venue.
- Mumbai Indians have won *54%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Mumbai Indians
Match Winner:* Gujarat Titans
-------------------------------------------------------------------------------------------

## Match 10: Delhi Capitals vs Sunrisers Hyderabad

*Date:* March 30, 2025\
*Venue:* ACA-VDCA Cricket Stadium,Visakhapatnam

###  Insights from Historical Data

- Delhi Capitals have won *44%* of matches since 2008-2024
- Sunrisers Hyderabad have won *47%* of matches since 2013-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 11: Rajasthan Royals vs Chennai Super Kings

*Date:* March 30, 2025\
*Venue:* Barsapara Stadium, Guwahat

###  Insights from Historical Data

- Rajasthan Royals have won *54%* of tosses since 2008-2024
- Rajasthan Royals have won *50%* of matches since 2008-2024
- Chennai Super Kings have won *58%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Rajasthan Royals
Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 12: Mumbai Indians vs Kolkata Knight Riders

*Date:* March 30, 2025\
*Venue:* Wankhede Stadium, Mumbai 

###  Insights from Historical Data

- Kolkata Knight Riders have won *55%* of tosses at this venue.
- Kolkata Knight Riders have won *32%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Mumbai Indians
Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 13: Lucknow Super Giants vs Punjab Kings

*Date:* April 01, 2025\
*Venue:* Ekana Cricket Stadium B Ground, Lucknow

###  Insights from Historical Data

- Lucknow Super Giants have won *25%* of tosses at this venue.
- Punjab Kings have won *25%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Punjab Kings
Match Winner:* Lucknow Super Giants

-------------------------------------------------------------------------------------------

## Match 14: Royal Challengers Bangalore vs Gujarat Titans

*Date:* April 02, 2025\
*Venue:* M. Chinnaswamy, Bengluru

###  Insights from Historical Data

- Royal Challengers Bangalore have won *33%* of tosses at this venue.
- Gujarat Titans have won *66%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Royal Challengers Bangalore
Match Winner:* Gujarat Titans

-------------------------------------------------------------------------------------------

## Match 15: Sunrisers Hyderabad vs Kolkata Knight Riders

*Date:* , April 03 2025\
*Venue:* Eden Gardens , Kolkata

###  Insights from Historical Data

- Sunrisers Hydrabad have won *57%* of tosses at this venue.
- Kolkata Knight Riders have won *67%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Sunrisers Hyderabad
 Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 16: Lucknow Super Giants vs Mumbai Indians

*Date:* April 04, 2025\
*Venue:* Ekana Cricket Stadium B Ground, Lucknow

###  Insights from Historical Data

- Mumbai Indians have won *83%* of tosses at this venue.
- Lucknow Super Giants have won *83%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Mumbai Indians
 Match Winner:* Lucknow Super Giants

-------------------------------------------------------------------------------------------

## Match 17: Chennai Super Kings vs Delhi Capitals

*Date:* April 05, 2025\
*Venue:* MA Chidambaram Stadium, Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *50%* of tosses at this venue.
- Chennai Super Kings have won *58%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
Match Winner:* Chennai Super Kings

------------------------------------------------------------------------------------

## Match 18: Rajasthan Royals vs Punjab Kings

*Date:* April 05, 2025\
*Venue:* Maharaja Yadavindra Singh International Cricket Stadium, New Chandigarh

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- - Punjab Kings have won *25%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Punjab Kings
Match Winner:* Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 19: Sunrisers Hyderabad vs Gujarat Titans

*Date:* April 06, 2025\
*Venue:* Rajiv Gandhi International Cricket Stadium, Hyderabad

###  Insights from Historical Data

- Sunrisers Hyderabad have won *55%* of tosses at this venue.
- Gujarat Titans have won *32%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Sunrisers Hyderabad
Match Winner:* Sunrisers Hyderabad

-------------------------------------------------------------------------------------------

## Match 20: Mumbai Indians vs Royal Challengers Bangalore

*Date:* April 07, 2025\
*Venue:* Wankhede Stadium , Mumbai 

###  Insights from Historical Data

- Mumbai Indians have won *55%* of tosses at this venue.
- Royal Challengers Bangalore have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Mumbai Indians
Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 21: Kolkata Knight Riders vs Lucknow Super Giants

*Date:* April 08, 2025\
*Venue:* Eden Gardern , Kolkata

###  Insights from Historical Data

- Kolkata Knight Riders have won *55%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Lucknow Super Giants have won *45%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Lucknow Super Giants
Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 22: Punjab Kings vs Chennai Super Kings

*Date:* April 08, 2025\
*Venue:* Maharaja Yadavindra Singh International Cricket Stadium , New Chandigarh

###  Insights from Historical Data

- Punjab Kings have won *44%* of matches since 2008-2024
- Chennai Super Kings have won *57%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Chennai Super Kings
Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 23: Gujarat Titans vs Rajasthan Royals

*Date:* April 09, 2025\
*Venue:* Narendra Modi Stadium , Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *45%* of tosses at this venue.
- Rajasthan Royals have won *49%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Rajasthan Royals
Match Winner:* Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 24: Royal Challengers Bangalore vs Delhi Capitals

*Date:* April 10, 2025\
*Venue:* M. Chinnaswamy Stadium , Bengaluru

###  Insights from Historical Data

- Royal Challengers Bangalore have won *33%* of tosses at this venue.
- Delhi Capitals have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 25: Chennai Super Kings  Kolkata Knight Riders

*Date:* April 11, 2025\
*Venue:* MA Chidambaram Stadium , Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *50%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Kolkata Knight Riders
Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 26: Lucknow Super Giants  vs Gujarat Titans

*Date:* April 12, 2025\
*Venue:* Ekana Cricket Stadium B Ground , Lucknow

###  Insights from Historical Data

- Gujarat Titans have won *55%* of tosses at this venue.
- Lucknow Super Giants have won *45%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Gujarat Titans
 Match Winner:* Gujarat Titans

-------------------------------------------------------------------------------------------

## Match 27: Sunrisers Hyderabad vs Punjab Kings

*Date:* April 12, 2025\
*Venue:* Rajiv Gandhi International Stadium , Hyderabad

###  Insights from Historical Data

- Sunrisers Hyderabad have won *56%* of tosses at this venue.
- Punjab Kings have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Punjab Kings
 Match Winner:* Sunrisers Hyderabad

-------------------------------------------------------------------------------------------

## Match 28: Rajasthan Royals vs Royal Challengers Bangalore

*Date:* April 13, 2025\
*Venue:* Sawai Mansingh Stadium , Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *50%* of tosses at this venue.
- Royal Challengers Bangalore have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:* Rajasthan Royals

------------------------------------------------------------------------------------

## Match 29: Delhi Capitals vs Mumbai Indians

*Date:* April 13, 2025\
*Venue:* Arun Jaitley Stadium , Delhi

###  Insights from Historical Data

- Mumbai Indians have won *54%* of matches since 2008-2024
- Delhi Capitals have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 30: Lucknow Super Giants vs Chennai Super Kings

*Date:* April 14, 2025\
*Venue:* Ekana Cricket Stadium B Ground , Lucknow

###  Insights from Historical Data

- Lucknow Super Giants have won *55%* of tosses at this venue.
- Chennai Super Kings have won *57%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Lucknow Super Giants
Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 31: Punjab Kings vs Kolkata Knight Riders

*Date:* April 15, 2025\
*Venue:* Maharaja Yadavindra Singh International Cricket Stadium , New Chandigarh

###  Insights from Historical Data

- Punjab Kings have won *55%* of tosses at this venue.
- Punjab Kings have won *44%* of matches since 2008-2024
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Punjab Kings
Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 32: Rajasthan Royals vs Delhi Capitals

*Date:* April 16 , 2025\
*Venue:* Arun Jaitly , Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Delhi Capitals have won *38%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
 Match Winner:* Rajasthan Royals 

-------------------------------------------------------------------------------------------

## Match 33: Mumbai Indians vs Sunrisers hyderabad

*Date:* April 17, 2025\
*Venue:* Wankhede Stadium , Mumbai

###  Insights from Historical Data

- Sunrisers Hyderabad have won *37%* of tosses at this venue.
- Mumbai Indians have won *54%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Mumbai Indians
Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 34: Royal Chellengers Bangalore vs Punjab Kings

*Date:* April 18, 2025\
*Venue:*  M Chinnaswamy Stadium , Bengaluru

###  Insights from Historical Data

- Royal Challengers Bangalore have won *65%* of tosses at this venue.
- Punjab Kings have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Royal challengers Bangalore
Match Winner:* Punjab Kings

-------------------------------------------------------------------------------------------

## Match 35: Gujarat Titans vs Delhi Capitals

*Date:* April 19, 2025\
*Venue:* Narendra Modi Stadium , Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *61%* of matches since 2008-2024 at this venue.
- Delhi Capitals have won *38%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Delhi Capitals
Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 36: Rajasthan Royals vs Lucknow Super Giants

*Date:* April 19, 2025\
*Venue:* Sawai Mansingh Stadium , Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Lucknow Super Giants have won *54%* of matches since 20022-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Rajasthan Royals
Match Winner:* Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 37: Punjab Kings vs Royal Challlengers Bangalore

*Date:* April 20, 2025\
*Venue:* Maharaja Yadavindra Singh International Cricket Stadium , New Chandigarh

###  Insights from Historical Data

- Punjab Kings have won *40%* of tosses at this venue.
- Royal Challengers Bangalore have won *38%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Punjab Kings
Match Winner:* Royal Challengers Bangalore

-------------------------------------------------------------------------------------------

## Match 38: Mumbai Indians vs Chennai Super Kings

*Date:* April 20, 2025\
*Venue:* Wankhede Stadium , Mumbai

###  Insights from Historical Data

- Mumbai Indians have won *65%* of tosses at this venue.
- Chennai Super Kings have won *55%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Mumbai Indians
Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 39: Gujarat Titans vs Kolkata Knight Riders

*Date:* April 21, 2025\
*Venue:* Eden Garden , kolkata

###  Insights from Historical Data

- Gujarat Titans have won *45%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Gujarat Titans
Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 40: Lucknow Super Giants vs Delhi Capitals

*Date:* April 22, 2025\
*Venue:* Ekana Cricket Stadium , Lucknow 

###  Insights from Historical Data

- Lucknow Super Giants have won *46%* of tosses at this venue.
- Delhi Capitals have won *38%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Lucknow Super Giants
Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 41: Sunrisers Hyderabad vs Mumbai Indians

*Date:* April 23, 2025\
*Venue:* Rajiv Gandhi Internaional Stadium , Hyderabad

###  Insights from Historical Data

- Sunrisers Hyderabad have won *56%* of tosses at this venue.
- Mumbai Indians have won *54%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Sunrisers Hyderabad
 Match Winner:* Sunrisers Hyderabad

-------------------------------------------------------------------------------------------

## Match 42: Royal Challengers Bangalore vs Rajasthan Royals

*Date:* April 24, 2025\
*Venue:* M . Chinnaswamy Stadium , Bengaluru

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Royal Challengers Bangalore have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:* Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 43: Chennai Super Kings vs Sunrisers Hydrabad

*Date:* April 25, 2025\
*Venue:* MA Chidambaram Stadium , Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *65%* of tosses at this venue.
- Sunrisers Hyderabad have won *48%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Chennai Super Kings
 Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 44: Punjab Kings vs Kolkata Knight Riders

*Date:* April 26, 2025\
*Venue:* Eden Gardens, Kolkata

###  Insights from Historical Data

- Punjab Kings have won *44%* of matches since 2008-2024
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Punjab Kings
 Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 45: Mumbai Indians vs Lucknow Super Giants

*Date:* April 27, 2025\
*Venue:* Wankhede Stadium , Mumbai

###  Insights from Historical Data

- Mumbai Indians have won *65%* of tosses at this venue.
- Lucknow Super Giants have won *54%* of matches since 20022-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Mumbai Indians
 Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 46: Delhi Capitals vs Royal Challengers Bangalore

*Date:* April 27, 2025\
*Venue:* Arun Jaitly Stadium, Delhi

###  Insights from Historical Data

- Delhi Capitals have won *48%* of tosses at this venue.
- Royal Challengers Bangalore have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Delhi Capitals
 Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 47: Rajasthan Royals vs Gujarat Titans

*Date:* April 28, 2025\
*Venue:* Sawai Mansingh Stadium, Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Gujarat Titans have won *62%* of matches since 2022-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:* Gujarat Titans

-------------------------------------------------------------------------------------------

## Match 48: Delhi Capitals vs Kolkata Knight Riders

*Date:* April 29, 2025\
*Venue:* Arun jaitley, Delhi

###  Insights from Historical Data

- Delhi Capitals have won *49%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Kolkata Knight Riders
 Match Winner:* Delhi Capitals

-------------------------------------------------------------------------------------------

## Match 49: Chennai Super Kings vs Punjab Kings

*Date:* April 30, 2025\
*Venue:* MA Chidambaram Stadium, Chennai

###  Insights from Historical Data

- Chennai Super Kings have won *55%* of tosses at this venue.
- Punjab Kings have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Punjab Kings
 Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 50: Rajasthan Royals vs Mumbai Indians

*Date:* May 01, 2025\
*Venue:* Sawai Mansingh Stadium, Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Mumbai Indians have won *54%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* MUmbai Indians
 Match Winner:*Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 51: Gujarat Titans vs Sunrisers Hyderabad

*Date:* May 02, 2025\
*Venue:* Narendra Modi Stadium, Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *58%* of tosses at this venue.
- Sunrisers Hyderabad have won *47%* of matches since 2013-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Gujarat Titans
 Match Winner:* Sunrisers Hyderabad

-------------------------------------------------------------------------------------------

## Match 52: Royal Challengers Bangalore vs Chennai Super Kings

*Date:* May 03, 2025\
*Venue:* M . Chinnaswamy Stadium, Bengaluru

###  Insights from Historical Data

- Chennai Super Kings have won *49.5%* of tosses at this venue.
- Royal Challengers Bangalore have won *49%* of matches since 2008-2024
- Teams batting first have a *60%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Chennai Super Kings
 Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 53: Rajasthan Royals vs Kolkata Knight Riders

*Date:* May 04, 2025\
*Venue:* Eden Gardens, Kolkata

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 54: Punjab Kings vs Lucknow Super Giants

*Date:* May 04, 2025\
*Venue:* HPCA Stadium

###  Insights from Historical Data

- Punjab Kings have won *44%* of matches since 2008-2024
- Lucknow Super Giants have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Lucknow Super Giants
 Match Winner:* Punjab Kings

-------------------------------------------------------------------------------------------

## Match 55: Sunrisers Hyderabad vs Delhi capitals

*Date:* May 05, 2025\
*Venue:* Rajiv Gandhi International Cricket Stadium

###  Insights from Historical Data

- Sunrisers HYderabad have won *48%* of tosses at this venue.
- Delhi Capitals have won *38%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Delhi Capitals
 Match Winner:* Sunrisers Hyderabad

-------------------------------------------------------------------------------------------

## Match 56: Mumbai Indians vs Gujarat Titans

*Date:* May 06, 2025\
*Venue:* Wankhede Stadium , Mumbai

###  Insights from Historical Data

- MUmbai Indians have won *58%* of tosses at this venue.
- Gujarat Titans have won *37%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Gujarat Titans
 Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 57: Chennai Super Kings vs Kolkata Knight Riders

*Date:* May 07, 2025\
*Venue:* Eden Gardens, Kolkata

###  Insights from Historical Data

- Vhennai Super Kings have won *48%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Kolkata Knight Riders
 Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 58: Punjab Kings vs Delhi Capitals

*Date:* May 08, 2025\
*Venue:* HPCA Stadium

###  Insights from Historical Data

- Delhi Capitals have won *49%* of tosses at this venue.
- Punjab Kings have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Delhi Capitals
 Match Winner:* Punjab kIngs

-------------------------------------------------------------------------------------------

## Match 59: Lucknow Super Giants vs Royal Challengers Bangalore

*Date:* May 09, 2025\
*Venue:* Ekana Cricket Stadium

###  Insights from Historical Data

- Lucknow Super Giants have won *48%* of tosses at this venue.
- Royal Challengers Bangalore have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Lucknow Super Giants
 Match Winner:* Royal Challengers Bangalore

-------------------------------------------------------------------------------------------

## Match 60: Sunrisers Hyderabad vs Kolkata Knight Riders

*Date:* May 10, 2025\
*Venue:*Rajiv Gandhi International Cricket Stadium

###  Insights from Historical Data

- Sunrisers Hydrabad have won *56%* of tosses at this venue.
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Kolkata Knight Riders
 Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 61: Punjab Kings vs Mumbai Indians

*Date:* May 11, 2025\
*Venue:* HPCA Stadium 
###  Insights from Historical Data

- Punjab Kings  have won *44%* of matches since 2008-2024
- Mumbai Indians have won *54%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Punjab Kings
 Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 62: Delhi Capitals vs Gujarat Titans

*Date:* May 11, 2025\
*Venue:* Arun Jaitley Stadium

###  Insights from Historical Data

- Delhi Capitals have won *38%* of matches since 2008-2024
- Gujarat Titans have won *60* of matches since 2022-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Delhi Capitals
 Match Winner:* Delhi capitals

-------------------------------------------------------------------------------------------

## Match 63: Rajasthan Royals vs Chennai Super Kings

*Date:* May 12, 2025\
*Venue:* MA Chidambaram Stadium

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Chennai Super Kings have won *57%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:*Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 64: Royal Challegers Bangalore vs Sunrisers Hyderabad

*Date:* May 13, 2025\
*Venue:* M Chinnaswamy Stadium

###  Insights from Historical Data

- Royal Challegers Bangalore have won *56%* of tosses at this venue.
- Sunrisers Hyderabad have won *47%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Sunrisers Hyderabad
 Match Winner:* Royal Challengers Bangalore

-------------------------------------------------------------------------------------------

## Match 65: Gujarat Titans vs Lucknow Super Giants

*Date:* May 14, 2025\
*Venue:* Narendra Modi Stadium , Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *49%* of tosses at this venue.
- Lucknow Super Giants have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Gujarat Titans
 Match Winner:* Gujarat Titans

-------------------------------------------------------------------------------------------

## Match 66: Mumbai Indians vs Delhi Capitals

*Date:* May 15, 2025\
*Venue:* Wankhede Stadium , Mumbai

###  Insights from Historical Data

- Mumbai Indians have won *56%* of tosses at this venue.
- Delhi Capitals have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Delhi Capitals
 Match Winner:* Mumbai Indians

-------------------------------------------------------------------------------------------

## Match 67: Rajasthan Royals vs Punjab Kings

*Date:* May 16, 2025\
*Venue:* Sawai Mansingh Stadium , Jaipur

###  Insights from Historical Data

- Rajasthan Royals have won *55%* of tosses at this venue.
- Punjab Kings have won *44%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Rajasthan Royals
 Match Winner:* Rajasthan Royals

-------------------------------------------------------------------------------------------

## Match 68: Royal Challengers Bangalore vs Kolkata Knight Riders

*Date:* May 17, 2025\
*Venue:* M . Chinnaswamy Stadium , Bengaluru

###  Insights from Historical Data

- Royal Challengers Bangalore have won *47%* of matches since 2008-2024
- Kolkata Knight Riders have won *51%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

 Toss Winner:* Royal Challengers Bangalore
 Match Winner:* Kolkata Knight Riders

-------------------------------------------------------------------------------------------

## Match 69: Gujarat Titans vs Chennai Super Kings

*Date:* May 18, 2025\
*Venue:* Narendra Modi Stadium , Ahmedabad

###  Insights from Historical Data

- Gujarat Titans have won *55%* of tosses at this venue.
- Chennai Super Kings have won *57%* of matches since 2008-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

*Toss Winner:* Gujarat Titans
*Match Winner:* Chennai Super Kings

-------------------------------------------------------------------------------------------

## Match 70: Lucknow Super Giants vs Sunrisers Hydrabad

*Date:* May 18, 2025\
*Venue:* Ekana Cricket Stadium , Lucknow

###  Insights from Historical Data

- Lucknow Super Giants have won *49%* of tosses at this venue.
- Sunrisers Hyderabad have won *47%* of matches since 2013-2024
- Teams batting first have a *50%* win rate at this venue.

###  Model Predictions

Toss Winner:* Sunrisers HYderabad
Match Winner:* Lucknow Super Giants

-------------------------------------------------------------------------------------------
#### PLAY-OFF MATCHES ####

## Match 71: TBD vs TBD 

*Date:* May 20, 2025\
*Venue:* Rajiv Gandhi International Cricket Stadium , Hyderabad

--------------------------------------------------------------------------------------------

## Match 72: TBD vs TBD

*Date:* May 21 , 2025
*Venue:* Rajiv Gandhi International Cricket Stadium , Hyderabad

---------------------------------------------------------------------------------------------

## Match 73: TBD vs TBD

*Date* May 23, 2025
*Venue:* Eden Gardens , Kolkata

----------------------------------------------------------------------------------------------

## Match 74: TBD vs TBD

*Date:* May 25, 2025
*Venue:* Eden Gardens , Kolkata