# Aspect-Based-Sentimental-Analysis
Aspect Based Sentiment Analysis (ABSA) is a technique that takes into consideration the terms related to the aspects and identifies the sentiment associated with each aspect. ABSA model requires aspect categories and its corresponding aspect terms to extract sentiment for each aspect from the text corpus. One can create a domain-specific model for a specific implementation; however, general language models can also be used.

Read the input file and extract the reviews text. After that, text may contain special characters, numeric data and many unwanted text that need to be removed in pre-processing steps.

After Pre processing, based on the aspect categories present in the input file given in config file, we will retrieve the polarity of the sentences.
Example - 
Sentence - burger is good but the service was dissapointing.
Output: {'food:burger': ('good', 1), 'service:service': ('dissapointing', -1)}

For positve review the value assigned to the aspect term determined by using POS tagging of NLP will be 1, and for negative reviews, it will be -1.

Finally, creating a dictonary, in order to save the number of apperances of each aspect category respective of positive and negative sentiments.
For example - 
positive_plot_dict {'ambience': 54, 'service': 47, 'food': 97, 'staff': 23, 'price': 2}
negative_plot_dict {'ambience': -17, 'service': -21, 'food': -40, 'staff': -5}

Using this data we can easily plot a side by side bar graph, which will give a visual idea about the reviews given.

NOTE - As here we are taking input file as restaurant reviews, aspect categories were related to restaurant, which can be changed in config file, depending on the input file given.

How to run------------
First set your virtual environment using the given absa.yaml file
Then run the Preprocessing.ipynb file.
Then run the config.ipynb file if any changes are made.
Then run the Analysis,ipynb file.
Then finally run the Sentimental Analysis.ipynb file to get the desired output.


