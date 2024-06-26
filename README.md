
# Career aspirations survey analysis

A career aspirations survey gathers information about the goals and aspirations of people in their careers. This will help you through Career aspirations survey analysis using plotly one of the Python library used for data visualization through graphs.




## Main objective


The information gathered from a career aspirations survey helps in understanding an individual’s:

1.long term goals

2.preferred work environment

3.preferred role and responsibilities

4.interests and values


## Documentation

You can download the dataset here:

[Career aspirations survey](https://www.kaggle.com/datasets/chandana1803/career-aspirations-survey)


## Deployment

To deploy this project run

```bash
import pandas as pd
import numpy as np
import plotly.express as px
import plotly.graph_objects as go

data = pd.read_csv("Your Career Aspirations of GenZ.csv")
print(data.head())
```
![Screenshot 2024-04-27 235046](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/26f16d47-b728-4190-af39-1e7cf0c9a2f5)
![Screenshot 2024-04-27 235106](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/4a5d5322-7b40-4610-83c4-8a388cc3b039)

Lets see all the questions 
```bash
print(data.columns)
```
![Screenshot 2024-04-28 001729](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/31ef06b6-0e77-4f3c-8232-d4f2d87ac7a8)

Lets analyse the current country question by pie chart
```bash
country = data["Your Current Country."].value_counts()
label = country.index
counts = country.values
colors = ['gold','lightgreen']
fig = go.Figure(data=[go.Pie(labels=label, values=counts)])
fig.update_layout(title_text='Current Country')
fig.update_traces(hoverinfo='label+value', textinfo='percent', textfont_size=30,
                  marker=dict(colors=colors, line=dict(color='black', width=3)))
fig.show()
```
![Screenshot 2024-04-28 001832](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/8a69cc68-e34e-4b82-b048-d33c82253510)

Lets analyse the same current country question by line graph

```bash
import plotly.graph_objs as go
country = data["Your Current Country."].value_counts()
label = country.index
counts = country.values

fig = go.Figure(data=go.Scatter(x=label, y=counts, mode='lines+markers', marker=dict(color='blue', size=10)))
fig.update_layout(title='Current Country', xaxis_title='Country', yaxis_title='Count')

fig.show()
```
![Screenshot 2024-04-24 230541](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/a70662c9-66ed-413a-9394-4d009dc0fe46)

Lets analyse "Which of the below factors influence the most about your career aspirations ?"

```bash
question1 = data["Which of the below factors influence the most about your career aspirations ?"].value_counts()
label = question1.index
counts = question1.values
colors = ['gold','lightgreen']
fig = go.Figure(data=[go.Pie(labels=label, values=counts)])
fig.update_layout(title_text='Factors influencing career aspirations')
fig.update_traces(hoverinfo='label+value', textinfo='percent', textfont_size=30,
                  marker=dict(colors=colors, line=dict(color='black', width=3)))
fig.show()
```
![Screenshot 2024-04-25 074925](https://github.com/Chandanaa18/career-aspirations-survey-analysis/assets/150374189/2577d4ff-32a1-49e2-81cb-cfccad02b5eb)


In the same way you can analyse for all the questions 
