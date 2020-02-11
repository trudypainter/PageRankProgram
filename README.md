# Readme

This python program applies Google\'92s PageRank algorithm to predictions for the most reportable event (MRE) of a story. It includes two ways to visualize the story data and effectively organizes and analyzes results.\
\
Instructions:\
\
Before you run:\
1. Make sure pagerank is saved in the same directory as the glove files and \reddit annotated folder\
2. Download glove files\
3. BEST RUN IN JUPYTER NOTEBOOK\
\
Functions:\
\
top3(index)\
- returns a list of the top3 predicted sentences using the PageRank algorithm\
- expects the index of the story being examined\
- top3(180) prints out the predicted indexes of the MRE in the story indexed at 180 in the reddit annotated data\
- in the example, the predicted MRE sentences are 4, 3, and 5\
EXAMPLE:\
top3(180)\
[4, 3, 5]\
\
checkIndex(storyid)\
- returns index of the story based on name of file from the annotated stories folder\
EXAMPLE\
checkIndex(\'93vfxbo.45.story\'94)\
28\
\
annotations(index)\
- returns a list of the ground truth annotated sentences\
- expects the index of the story being examined (like top3(index))\
- in the example, the ground truth sentence is 0\
EXAMPLE\
annotations(180)\
[0]\
\
linegraph(index)\
- returns a line graph (string) of the results\
- empty circles have neither a ground truth or predicted sentences. circles with top half filled have only predicted sentences. circles with bottom half filled have only ground truth sentences. completely filled circles have both.\
- expects the index of the story being examined\
EXAMPLE\
linegraph(180)\
\pard\pardeftab720\sl320\partightenfactor0

\f1\fs28 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 '
\f2 \uc0\u9682 \'81\'fc\'81\'fc\u9683 \u9683 \u9683 
\f1 '\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
visualizeGraph(index)\
- returns a graph of the ranked sentences\
- is not included in results csv - must be used in notebook or python\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 - expects the index of the story being examined\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 EXAMPLE\
visualizeGraph(180)\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f3 \cf2 \expnd0\expndtw0\kerning0
{{\NeXTGraphic unknown.png \width3320 \height4620 \appleattachmentpadding0 \appleembedtype0 \appleaqc
}¬}
\f0 \cf0 \kerning1\expnd0\expndtw0 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 \
printInfo(180)\
- prints all of the information using above methods\
- in my program, this is used o create a csv of all stories\'92 information\
- expects the index of the story being examined\
EXAMPLE\
printInfo(180)\
\pard\pardeftab720\sl320\partightenfactor0

\f1\fs28 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 180 | 1h7qys.44.story|  [0] |  [3, 4, 5]  | 
\f2 \uc0\u9682 \'81\'fc\'81\'fc\u9683 \u9683 \u9683 
\f1 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
get_pres_and_recall(results)\
- will print out the precision and recall of the data\
- expects a data table - see how to define it in code before\
EXAMPLE\
get_pres_and_recall(results_df)\
\pard\pardeftab720\sl320\partightenfactor0

\f1\fs28 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 pres:0.19420289855072465 recall:0.27714581178903824\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \cb1 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
\
\pard\pardeftab720\sl280\partightenfactor0
\cf0 \
\pard\pardeftab720\sl280\partightenfactor0

\f3 \cf2 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 \
\

\f0 \cf0 \kerning1\expnd0\expndtw0 \outl0\strokewidth0 \
}
