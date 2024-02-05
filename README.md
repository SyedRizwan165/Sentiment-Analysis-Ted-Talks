# Sentiment-Analysis-Ted-Talks
This repository contains a comprehensive analysis of two TED Talks delivered by different speakers, Jim Holt and Nathaniel Kahn. The goal of this analysis is to delve into the content of these talks, extracting insights through various techniques such as word frequency identification, sentiment analysis, and visualizations.

## Data Tidying and Tokenization
The initial dataset, named "MyData," presented the TED Talks in an untidy text format. The first step involved tidying and tokenizing the data using the unnest_tokens() function from the tidytext package. This process transformed the data into a tidy format with one token per row, resulting in the creation of the "MyData_tidy" dataset.

## Stop Words Removal
To enhance the analysis, common stop words were removed using the tidytext package's get_stopwords() function combined with dplyr's anti_join(). The cleaned dataset was then stored in a new variable named "MyData_stop_words."

## Identification and Visualization of Top Words
The analysis identified the most frequently used words by each speaker, visualizing them through bar charts. The top words were determined using the count function from the dplyr package, and the results were plotted using the ggplot2 library.

## Comparing Speaker Words Using Visualization
To provide a visual comparison between the speakers, only words with a cumulative frequency across both talks exceeding 10 times were selected. The ggplot2 package, specifically the geom_text_repel() function from ggrepel, facilitated the plotting of Jim Holt's words on the x-axis against Nathaniel Kahn's words on the y-axis.

## Calculating Odd-Ratio
For a deeper analysis, odd ratios were calculated to measure the strength of association between specific words and sentiments. The dsEssex package's compute_OR function was employed to determine the odd ratios, and the results were transformed into a more interpretable scale by calculating the logarithm of the odd ratio.

## Sentiment Analysis
The final step involved sentiment analysis using the "bing" lexicon of Hu and Liu (2004). The get_sentiments("bing") function was utilized for sentiment categorization, followed by the calculation of positive and negative word percentages for each talk. The most common positive and negative words for both speakers were identified and visualized using geom_col() and facet_wrap().

This repository offers a comprehensive exploration of the TED Talks' content, providing valuable insights into the themes, sentiments, and word choices of speakers Jim Holt and Nathaniel Kahn. Feel free to explore the code and visualizations to gain a deeper understanding of the narratives presented in these talks.
