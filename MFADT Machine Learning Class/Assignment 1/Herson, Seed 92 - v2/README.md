### Strategies

#### Previous
[ ] Testing with a matrix of features that only includes:
    [ ] Word count, per review
    [ ] Count of exclamation points
    
This was just to get back to a baseline, where accuracy and precision were roughly ~0.5.
Previous strategies where I included these two features + vectorization of reviews were causing
accuracy and precision to jump all the way to 1.0 for most models on the training set, but 
around 0.83 for the test set.

#### Current
[/] Cleaning reviews
    [/] Removed all non-alphabetical characters, except of `!`
    [/] Lowercased all characters
    [/] Applied a frequency threshold to identify unique words
    [/] Filtered out stop words, filtered by unique words
    [/] Applied stemming
[/] Stacked matrix of features that includes vectorization of filtered, cleaned reviews +
    number of words + number of exclamation
    