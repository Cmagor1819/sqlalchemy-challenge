# sqlalchemy-challenge

# Objective:

### Part 1:

This section's purpose is to use Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database. Specifically, using SQLAlchemy ORM queries, Pandas, and Matplotlib. This section is reflecting the tables of the database into SQLAlchemy ORM and then performing an exploratory precipiation and station analysis. 

### Exploratory Precipitation Analysis:

This section is finding the most recent date in the data set, desinging a query to retrieve the last 12 months of precipitation and plotting the results with Matplotlib.

### Exploratory Station Analysis

This section is designing queries to calculate the total number of stations, finding the most active stations, and calculating the lowest, highest, and average temperatures. We then take that info and query the last 12 months of temp observation data and plot it on a histogram. 

Finalized this part by making sure to close out of the session with session.close()

### Part 2:

This section's purpose is to design the climate app and create a Flask API based on the queries that were just developed. We import all the dependencies and set up the rest of the page.

### Database Setup:

This section is creating an engine to hawaii.sqlite and reflecting an existing database into a new model. We then reflect the tables from said database and save references to each of those tables.

### Flask Setup:

This section is creating the flask app and defines a function that calculates and returns the date one year from the most recent date.

### Flask Routes:

This section is setting up all the different routes and what to do when the user reaches a certain page/URL. In this section we are defining what to do when the user reaches the home page, precipitation URL, station URL, tobs URL, URL with a specific start date, and a URL with a specific start-end rage. We then create lists to store dictionaries containing data from specific objects, jsonify those lists, and then return them.

We make sure to finalize this part by closing the session with session.close()

### The following lines of code were referenced from Xpert Learning Assistant/GitHub:

most_recent = session.query(Measurement.date).order_by(Measurement.date.desc()).first()

lowest_temp = session.query(func.min(Measurement.tobs)).filter(Measurement.station == 'USC00519281').first()

most_recent = session.query(func.max(Measurement.date)).first()[0]
    first_date = dt.datetime.strptime(most_recent, "%Y-%m-%d") - dt.timedelta(days=365)

station_list = list(np.ravel(station_data))

for min, avg, max in start_date_tobs:
start_date_tobs_dict = {}

if end == None:
    start_data = session.query(*temp_list).filter(Measurement.date >= start).all()

def new_func(session):
    session.close()
    new_func(session)


    

    
