# Museum feedback aggregator

<div>
    <a href="https://colab.research.google.com/drive/1bTzcYtYd8e_MKMB0qU6J2f7tPGWFSjdO#scrollTo=ZVR4VY_nI81w"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
</div>

## About project
It's a little solution to compare some museums with each other. It is implemented by aggregating museum reviews, determining them sentiment and extracting keyphrases.  
[Pitching presentation](https://docs.google.com/presentation/d/1OKsV8XCdAYj2QRS6BV3_5bGBb55pnsHL/edit#slide=id.p1)  

Example of output of museum review:
![](/src/rating.png)
![](/src/sentiment.png)
![](/src/wordcloud.png)
For sentiment determining we use [rubert-base-cased-sentiment model](https://huggingface.co/blanchefort/rubert-base-cased-sentiment)   
For keyphrases extraction we use [keyt5-base model](https://huggingface.co/0x7194633/keyt5-base) 

## Get starting
The easiest way to reproduce the solution is to open colab, switch on GPU mode, load museum_feedback.xlsx dataset and start all notebook.  
You can run notebook local. To do this you should install all dependencies, like pandas and torch. And probably you'll need GPU to run this code.  

## Dataset
We collected the dataset manually from the Yandex maps website  
![](/src/data_resource.png)
Dataset stored in data folder and look like this:

| museum_id | feedback_text       | visitor_mark  | museum_name |
|-----------|---------------------| ------------- | ------------- |
| 1         | Отличный музей, ... |      5     |     Музей истории Томска      |
