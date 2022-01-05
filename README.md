### Understand Text Summarization and create your own summarizer in python

We all interact with applications which uses text summarization. Many of those applications are for the platform which publishes articles on daily news, entertainment, sports. With our busy schedule, we prefer to read the summary of those article before we decide to jump in for reading entire article. Reading a summary help us to identify the interest area, gives a brief context of the story.

![image](https://user-images.githubusercontent.com/76062756/148164444-12d45962-df40-47ab-8d88-db50c06eb571.png)

Summarization can be defined as a task of producing a concise and fluent summary while preserving key information and overall meaning.

#### Impact:

Summarization systems often have additional evidence they can utilize in order to specify the most important topics of document(s). For example, when summarizing blogs, there are discussions or comments coming after the blog post that are good sources of information to determine which parts of the blog are critical and interesting.
In scientific paper summarization, there is a considerable amount of information such as cited papers and conference information which can be leveraged to identify important sentences in the original paper.

How text summarization works:

In general there are two types of summarization, abstractive and extractive summarization.
#### Abstractive Summarization:
Abstractive methods select words based on semantic understanding, even those words did not appear in the source documents. It aims at producing important material in a new way. They interpret and examine the text using advanced natural language techniques in order to generate a new shorter text that conveys the most critical information from the original text.
Input document → understand context → semantics → create own summary

### 2. Extractive Summarization: 
Extractive methods attempt to summarize articles by selecting a subset of words that retain the most important points
Input document → sentences similarity → weight sentences → select sentences with higher rank.

### Next, Below is our code flow to generate summarize text:-

Input article → split into sentences → remove stop words → build a similarity matrix → generate rank based on matrix → pick top N sentences for summary.

### How to run:
1.Clone the repository with cmd: git clone 
2.Setup the virtual environment and activate it
3.Install the requirements using cmd: pip install -r requirements.txt
4.Run the application using cmd: python text-summarizer.py

well finished,you can see result in the terminal.

### Let’s look at it in action.
### The complete text from an article titled Microsoft Launches Intelligent Cloud Hub To Upskill Students In AI & Cloud Technologies
suppose the input file is msft.txt 
and the summarized text with 2 lines as an input is

Envisioned as a three-year collaborative program, Intelligent Cloud Hub will support around 100 institutions with AI infrastructure, course content and curriculum, developer support, development tools and give students access to cloud and AI services. The company will provide AI development tools and Azure AI services such as Microsoft Cognitive Services, Bot Services and Azure Machine Learning. According to Manish Prakash, Country General Manager-PS, Health and Education, Microsoft India, said, "With AI being the defining technology of our time, it is transforming lives and industry and the jobs of tomorrow will require a different skillset.

### Conclusion:
As you can see, it does a pretty good job. You can further customized it to reduce to number to character instead of lines.

It is important to understand that we have used textrank as an approach to rank the sentences. TextRank does not rely on any previous training data and can work with any arbitrary piece of text. TextRank is a general purpose graph-based ranking algorithm for NLP.
