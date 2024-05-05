# Misspelled-KG-dataset

This dataset is prepared based on [Kyrgyz_News_Corpus](https://huggingface.co/datasets/the-cramer-project/Kyrgyz_News_Corpus).

Preliminary processing has been carried out: 
1. All symbols that are absent in the Kyrgyz or Latin alphabets or numbers have been excluded.
2. 2. Various variants of dashes/hyphens have been replaced with a single type of dash, different variants of quotation marks have been replaced with a single type of quotation mark, and extra spaces have been removed.
3. Long news articles have been divided into lines so that mean(len) = 102.45 and std(len) = 56.72. 4. Rows with languages other than Kyrgyz have been excluded.

Misspelled (trash) text was created using various approaches: 
• 1 million trash lines were generated using a probabilistic noiser. The probabilistic noiser was trained based on a "golden dataset" with real errors, which is not public. 
• 500 thousand trash lines were generated using a different probabilistic [noiser](https://github.com/ai-forever/sage.git). 
• The remaining trash lines were created using a random noiser, which, for words longer than 5 letters, has a 20% probability of deleting a letter/swapping a letter/replacing a letter with another letter/inserting any letter.

Punctuation errors (punc_trash) text was created using a random noiser, which has a 20% probability of deleting/inserting a comma and replacing the period at the end of the sentence with another punctuation mark, such as "!" or "?".

Train and test datasets were created by train_test_split with a train size of 2 million: • Train size = 2000000 • Test size = 66223

# References
All of our achievements were made achievable thanks to the robust AI community in Kyrgyzstan and the contributions made by individuals within the AkylAI project (by TheCramer.com). We also express our gratitude to the Kyrgyz news agencies for their work, which allowed us to create this dataset.

# Next
We work on creation Kyrgyz Spell checker and grammar corrector. Please feel free to reach out timur.turat@gmail.com or rkizmailov@gmail.com if you are interested in any forms of collaborations!

# License
Dataset is licensed under a [Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/)
