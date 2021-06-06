# AwakeLabs Challenge

## How to run

1. Create a virtualenv
2. `pip install jupyterlab` or use another method of installation here: https://github.com/jupyterlab/jupyterlab'
3. Add the `data.json` file to the directory you're working in
4. Run `jupyter lab` which will open up the Jupyter Lab on localhost
5. Run the code blocks in order from top to bottom
6. Adjust the date and graph style in the makeGraph function call to create a graph at that specified date and whether you want the day's BPM to be shown or the week corresponding to it. Setting `is_day=True` will show the graph for that day, and `is_day=False` for the week.

## Write Up

#### How I dealt with the json:

I loaded the json file normally into python and made an array of all the rows of data

I decided to use pandas in order to store and manipulate the data. I used pandas because:
- Better performance over numpy on larger datasets which our provided dataset is and what AwakeLabs will deal with
- Uses DataFrame and Series data structures which have lots of features and integrations. DataFrame allows multiple columns and has json support to allow us to easily deal with nested JSON like being able to create a DataFrame table from different layers in a nested JSON. Series and DataFrame has easy integration with Bokeh which is the graphing tool I chose to use, so I don't need to export data myself from these sources and manipulate it to create a graph from it, it does it behind the scenes in an efficient way.
- Pandas is widely used so if AwakeLabs wanted to do something else with this data, there certainly exists a library/package/tool that has Pandas integration included so using this is very future proof
- As DataFrame is a table, we can easily access data in other columns and make more graphs
- Built in filtering which allows me to select only data rows within a certain date range and its abstracted so we don't have to worry about what's the best way to do that


