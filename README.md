# career-aspirations-survey-analysis
A career aspirations survey gathers information about the goals and aspirations of people in their careers. It includes questions based on long-term goals, preferred work environment, interests, and values. This will help you through Career aspirations survey analysis using Python.

Career Aspirations Survey Analysis
The information gathered from a career aspirations survey helps in understanding an individual’s:

long term goals
preferred work environment
preferred role and responsibilities
interests and values


importing libraries

import pandas as pd
import numpy as np
import plotly.express as px
import plotly.graph_objects as go

data = pd.read_csv("Your Career Aspirations of GenZ.csv")
print(data.head())
