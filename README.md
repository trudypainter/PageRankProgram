# README

This python program applies Google's PageRank algorithm to predictions for the most reportable event (MRE) of a story. It includes two ways to visualize the story data and effectively organizes and analyzes results.

## Instructions Before

Before you run:
1. Make sure pagerank is saved in the same directory as the glove files and \redditannotated folder
2. Download glove files (https://www.kaggle.com/terenceliu4444/glove6b100dtxt#glove.6B.100d.txt)
  - make sure to save file in same directory as pagerank program
3. Download annotated reddit dataset from (http://www.cs.columbia.edu/~ouyangj/reddit-data/)
  - rename folder as "redditannotated" and move union file to redditannotated folder
3. BEST RUN IN JUPYTER NOTEBOOK

## Functions
\
top3(index)
- returns a list of the top3 predicted sentences using the PageRank algorithm\
- expects the index of the story being examined\
- top3(180) prints out the predicted indexes of the MRE in the story indexed at 180 in the reddit annotated data
- in the example, the predicted MRE sentences are 4, 3, and 5\
EXAMPLE:\
top3(180)\
[4, 3, 5]

checkIndex(storyid)
- returns index of the story based on name of file from the annotated stories folder\
EXAMPLE\
checkIndex('vfxbo.45.story')\
28

annotations(index)
- returns a list of the ground truth annotated sentences
- expects the index of the story being examined (like top3(index))
- in the example, the ground truth sentence is 0\
EXAMPLE\
annotations(180)\
[0]

linegraph(index)
- returns a line graph (string) of the results
- empty circles have neither a ground truth or predicted sentences. circles with top half filled have only predicted sentences. circles with bottom half filled have only ground truth sentences. completely filled circles have both.
- expects the index of the story being examined\
EXAMPLE\
linegraph(180)\
◒◯◯◓◓◓

visualizeGraph(index)
- returns a graph of the ranked sentences
- is not included in results csv - must be used in notebook or python\
EXAMPLE
visualizeGraph(180)
see results in example image in folder

printInfo(180)
- prints all of the information using above methods
- in my program, this is used o create a csv of all stories' information
- expects the index of the story being examined\
EXAMPLE\
printInfo(180)\
180 | 1h7qys.44.story|  [0] |  [3, 4, 5]  | ◒◯◯◓◓◓

get_pres_and_recall(results)
- will print out the precision and recall of the data
- expects a data table - see how to define it in code before\
EXAMPLE\
get_pres_and_recall(results_df)\
pres:0.19420289855072465 recall:0.27714581178903824
