# Fetch_Exercise

## Run instructions 
To run the project, click on the 'Similarity.ipynb' file above, and then click 'open in collab.' You may be prompted to sign in to a google account, to run it, but I have made the project public, so you should be able to run it in that notebook. If you have any issues you may need to save the notebook as your own, or as a last resort copy and paste the code into a local python interpreter if your environement does not allow for the usage of Google-based development enironments. 

## My Thought Process 
Since the project specifications state that the similarity checker does not have to be practical / optimizaed, I thought I would take an interesting approach, one which reflects how I like to look at data when doing numerical analysis.

Also since 'similarity' is somewhat ambiguous, my goal became to implement a method which factors in proximity when checking for similarity. By this I mean that 'abc' is much more similar to 'cab' than 'zxy' because of the letter's proximity to each other lexicographically. 
The way I handled this was by coverting all of the characters (including punctuation) into their ASCII equivelants, and then converting that into an array. I then pad the arrays with average values for that array (I know, this is very unpractical but fun for the purposes of this exercise). With these averages I calculate the cosine similarity, which accounts for proximity due to the numerical convesion, but due to the unscaled nature of punctuation as ASCII values, and the fact that this is case sensitve, the accuracy is fairly unreliable. Though this could definitely be improved in terms of accuracy by disregarding punctuation and casing. 

As a final fun exercise, I wanted to represent similarity graphically. To do this, I took my arrays created in the steps above and plotted the lines over top of each other, this way you can look and see that when two strings are identical, they overlap perfectly. The huge spikes in this graphical represneation (check out the example below) depict the punctuation, as the ASCII values for punctation are quite far from the ASCII values for letters. 

## Example output: 
![example output for similarity checker](https://github.com/jacobarger/Fetch_Exercise/blob/main/output_1.png?raw=true)
