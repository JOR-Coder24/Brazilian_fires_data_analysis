import pandas as pd
import matplotlib.pyplot as plt
import plotly.express as px

data = pd.read_csv('brazilian_amazon_fires_1999_2019.csv')


print(data) #print all the data

df = pd.read_csv('brazilian_amazon_fires_1999_2019.csv', nrows=5)#print the first n rows of the file
print(df)
print("The most common state of the fires is ", data["state"].mode())#Finds the mode of states
print("The average number of firespots is ", data["firespots"].mean())
print("The median of firespots is ", data["firespots"].median())#median of firespots
print("Here is the average number of firespots by state:")
print(data[["state", "firespots"]].groupby("state").mean())# print mean of firespots by states
print("Here is the total number of firespots by state:")
print(data[["state", "firespots"]].groupby("state").sum())# print sum of firespots by state
print(data.isnull())# shows data is null


avg_firespots = data.groupby("state")["firespots"].mean().sort_values()#sorts state by ascending order in mean of firespots

# Plotting the bar chart
plt.figure(figsize=(10, 6))
avg_firespots.plot(kind='bar', color='red')

plt.xlabel('State')
plt.ylabel('Average Firespots')
plt.title('Average Firespots by State')
plt.xticks(rotation=45)

# Display the chart
plt.show()

fires=pd.read_csv("brazilian_amazon_fires_1999_2019.csv")
fig = px.density_mapbox(fires, lat='latitude', lon='longitude',z='firespots', radius=10,
                        center=dict(lat=0, lon=180), zoom=0,
                        mapbox_style="open-street-map")
fig.show()

print(data["firespots"].sum())#displays total sum of firespots
