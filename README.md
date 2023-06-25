# Ulysses NLP Analysis

## Introduction

This README provides an overview of the NLP analysis conducted on the novel "Ulysses" by James Joyce.
The analysis involves several tasks aimed at identifying the main voices (character names) and key terms, extracting definitory features of the characters, analyzing their interactions, hierarchically segmenting the text, and identifying rhetorical schemas within the novel.

## Identifying Voices and Key Terms

In this task, various NLP techniques are utilized to identify the main voices (character names) and key terms in the novel.
The techniques used include lemmatization, part-of-speech recognition (POS) and named entity recognition (NER).

1. Lemmatization: performed to reduce word variations and group similar words together, enhancing the semantic understanding of the text.

2. Part-of-Speech Recognition: assigned part-of-speech tags to each token in the text using the `pos_tag` function.
This helped in distinguishing character names (typically nouns) from other words.

3. Named Entity Recognition: used the spaCy library for named entity recognition to identify names of persons (PERSON) in the text. Only entities of interest were selected.

### Results - Character Names:

1. 'Joe' appears 115 times in the novel.
2. 'Dedalus' appears 98 times.
3. 'Stephen' appears 83 times.
4. 'Martin Cunningham' appears 70 times.
5. 'Conmee' appears 51 times.
6. 'Gerty' appears 49 times.
7. 'Ned Lambert' appears 39 times.

These character names are the main voices in the novel, indicating their significant roles and frequent mentions throughout the text.

### Results - Key Terms:

1. 'time' appears 412 times in the novel.
2. 'hand' appears 403 times.
3. 'man' appears 403 times.
4. 'eye' appears 396 times.
5. 'thing' appears 295 times.
6. 'day' appears 295 times.
7. 'way' appears 278 times.

These key terms represent important concepts or ideas that are frequently referenced in the novel.

## Extracting Definitory Features

The aim is to extract the definitory features (attributes) of the main voices in the novel. 
Dependency parsing is used and specific dependency relationships (e.g., adjective modifier -amod- and compound) to extract these features.

The main voices identified were iterated, and their occurrences in the text were matched using dependency parsing.
Definitory features were extracted based on the identified dependency relationships.

### Results:

Here are some examples of the definitory features extracted for the main voices:

- Voice: Joe
  - Definitory Features: ['holy', 'racing', 'little', 'sports', 'Decent', 'JOE', 'fellow']

- Voice: Dedalus
  - Definitory Features: ['Si', 'young', 'S.', 'little', 'surviving', 'Nameless', 'quay']

- Voice: Stephen
  - Definitory Features: ['prone', 'sir', 'Simon', 'ashplant', 'Stephen', 'young', 'middle']

- Voice: Gerty
  - Definitory Features: ['responded', 'threecornered', 'Mr', 'christmas', 'halcyon', 'young', 'delicate']

These definitory features provide insights into

 the distinctive attributes or characteristics associated with each voice in the novel.

## Analyzing Interactions between Voices

In this task, the interest is focused on identifying connections and interactions between the main voices in the novel.
Sentiment analysis and dependency parsing techniques are employed to determine the sentiment polarity and classify the interactions as agreement or disagreement.

The techniques used included:

1. SentimentIntensityAnalyzer: to determine the sentiment polarity of the interactions between characters.
Sentences indicating agreement or disagreement were analyzed.

3. Spacy Matcher: to define an interaction pattern based on the dependency relationship of a preposition between two character names.
Sentences containing both characters were matched against this pattern to identify interactions.

For the matched interactions, dependency parsing was performed to analyze the grammatical structure, and sentiment analysis was used to determine the sentiment polarity.

### Results:

Based on the analysis, the frequency of agreement interactions between different characters can be observed.
The following characters had a higher frequency of agreement interactions:

- Joe
- Dedalus
- Stephen
- Martin Cunningham
- Conmee

On the other hand, Ned Lambert had fewer agreement interactions compared to the other characters, suggesting more instances of disagreement or conflicting interactions with other characters.

## Hierarchical Segmentation of the Text

In this task, the text of the novel is hierarchically segmented into chapters, sections, paragraphs, groups of sentences, and short segments using XML annotations.

Using delimiters such as `chapter_delimiter`, `section_delimiter`, `paragraph_delimiter`, and `group_delimiter`, an XML structure is created to represent the hierarchical segments. 
The library `xml.etree.ElementTree` was used for creating the XML structure, and `xml.dom.minidom` was utilized to format the content for improved readability.

## Identifying Rhetorical Schemas

For this task, specifical rhetorical schemas presented in the novel are analyzed.

- Anaphora: the repetition of a word or phrase at the beginning of successive clauses.

- Antithesis: the juxtaposition of contrasting ideas or words to create a contrasting effect.

- Chiasmus: the reversal or crossing of structures in words or sentences.

The analysis provided examples and counts of occurrences for each rhetorical schema.

## Conclusion

The NLP analysis conducted on "Ulysses" by James Joyce involved several tasks, including identifying voices and key terms, extracting definitory features, analyzing interactions, hierarchically segmenting the text, and identifying rhetorical schemas. The results provided insights into the main characters, their attributes, interactions, and the rhetorical patterns present in the novel.
