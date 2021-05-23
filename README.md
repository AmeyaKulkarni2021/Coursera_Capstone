# Coursera_Capstone
# Searching for optimal locations for Cloud Kitchens in Mumbai
# Project is divided into 3 stages,

# Part 1 - Generating Datasets
# Part 2 - Search Space Creation
# Part 3 -  Optimal Location and Location Set Identification
# Part 4 -  Cuisine recommendations for best locations

# Approach:
# Our analysis is based on computing the distance betweent to location coordinates, and optimising the search using this are the key parameter.

# Distance is defined as the sum of the x(or W-E) and y (or N-S) intercept.

# The analysis progresses with first rating each venue location as follows, rating = (minimum service time for a given set of city centres)/(service time of a location for given set of city centres)

# This data will be used to train a model that can generate similar ratings for any point using the following three attributes,

# Number of city centres within serviceable distance
# Average distance between location and the city centres
# Average potential serviceable population
# Then we generate a search space of points using the city centre location coordinates, and find points with the best ratings.

# It is assumed that these points represent locations that have the maximum potential serviceable population for given set of city centres possible.

# After that top locations are sorted and searched for a combination of best locations that serve the maximum proportion of population of the city centres.

# Once we have obtained the list of best locations, we simply check the venue categories available at all city centres near our best locations.

# We use the Foursquare location data to compute the average venue category at each city centre, and then use the population of the city centres to compute the weighted average for a best location.

# Key comments
# We have two datasets for city centers, but one lacks population data, hence it is automatically dropped from further analysis
# Still we have utilised that data to generate venue locations from the Foursquare API as it provides more results
# Venue category or cuisine reccomendations are based Foursquare location data
# Functions for all computations will be available in related notebooks
