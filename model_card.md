# 🎧 Model Card: Music Recommender Simulation

## 1. Model Name  

**SoundFit 1.0**  

---

## 2. Intended Use  

Describe what your recommender is designed to do and who it is for. 

Prompts:  

- What kind of recommendations does it generate  
- What assumptions does it make about the user  
- Is this for real users or classroom exploration  

The recommender is designed to give users new song recommendations based on what they appreciate the most in music.

---

## 3. How the Model Works  

Explain your scoring approach in simple language.  

Prompts:  

- What features of each song are used (genre, energy, mood, etc.)  
- What user preferences are considered  
- How does the model turn those into a score  
- What changes did you make from the starter logic  

Avoid code here. Pretend you are explaining the idea to a friend who does not program.

The program will check on what the user likes that most in terms of the mood and genre of his songs, with other aspects. It looks into those values and gives suggestions of new songs that they might like.

---

## 4. Data  

Describe the dataset the model uses.  

Prompts:  

- How many songs are in the catalog  
- What genres or moods are represented  
- Did you add or remove data  
- Are there parts of musical taste missing in the dataset  

The model uses a dataset of 10 songs, with the title, genre, and moods being represented as strings and other parts in the set represented as percentages

---

## 5. Strengths  

Where does your system seem to work well  

Prompts:  

- User types for which it gives reasonable results  
- Any patterns you think your scoring captures correctly  
- Cases where the recommendations matched your intuition 

The system can identify a strong correlation on genre and mood. If they care both a match, then it is 60% more likely to be recommended

---

## 6. Limitations and Bias 

Where the system struggles or behaves unfairly. 

Prompts:  

- Features it does not consider  
- Genres or moods that are underrepresented  
- Cases where the system overfits to one preference  
- Ways the scoring might unintentionally favor some users  

Genre is an exact binary match worth 3 points — the single largest factor worth 30% of the overall scoring. A song in the user's preferred genre starts with a 3-point head start over every song outside it. 

---

## 7. Evaluation  

How you checked whether the recommender behaved as expected. 

Prompts:  

- Which user profiles you tested  
- What you looked for in the recommendations  
- What surprised you  
- Any simple tests or comparisons you ran  

No need for numeric metrics unless you created some.

For user profiles 3 and 4, i have experimented with the different aspects of the preferences. I have discovered that lofi genre gets associated highly with a chill mood, while pop is more associated with a happy mood.

---

## 8. Future Work  

Ideas for how you would improve the model next.  

Prompts:  

- Additional features or preferences  
- Better ways to explain recommendations  
- Improving diversity among the top results  
- Handling more complex user tastes  

The model can have a larger dataset with different data that have lower correlation than the current one.

---

## 9. Personal Reflection  

A few sentences about your experience.  

Prompts:  

- What you learned about recommender systems  
- Something unexpected or interesting you discovered  
- How this changed the way you think about music recommendation apps  

One thing that I learned about these recommenders is how almost all of them use mathmatical calculations on scoring and being almost inaccurate with what the user intends to find. Sure, keeping track of the user's favorite features in music is great, but what if the user wanted something completly different? What if he is making a playlist for different vibes and moods? I found it rather interesting how almost all systems rely on pure data consumptions and can be inaccurate with what a person may be looking for. 