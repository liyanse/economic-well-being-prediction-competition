# economic-well-being-prediction-competition
Can you predict a measure of wealth for different locations across Africa?
Granular information on economic well-being is extremely useful for governments, policy makers, and NGOs. 
But household surveys that capture this kind of information are expensive and conducted infrequently in many African countries. 
For this competition we will attempt to create a workaround for this lack of data by building a model able to predict a measure of wealth as measured in household surveys using readily available inputs.
Using data from 18 different countries collected at different times, you must correctly predict the cluster-level estimated wealth measures found from surveys in 7 different countries not covered in the training data. 
A successful model could be useful for filling in the gaps between the more expensive surveys.

The target is a derived ‘wealth index’ based on responses in various household surveys. It is on a scale from 0 to 1, with 1 denoting higher wealth. This measure is based on multiple factors such as asset ownership, and gives a single measure across the different surveys and countries that we can use to compare data points in a consistent way. Each row in the dataset corresponds to a cluster of survey responses, and so the Target is a measure of the average wealth for a given cluster of respondents.

For the solution to be applicable elsewhere, the inputs need to be derived from datasets with appropriate coverage. All of the datasets used cover the whole of Africa, meaning that any solution based on these can in theory be used to predict the wealth index for any country. Layers sampled include measures of human settlement, land cover and nighttime light emissions, as well as two distance measures that often relate to economic success: distance to the country’s capital and distance to the ocean. For many of these measures, the value given is the average for a 5km radius around the cluster center.

If, when you click to download the starter notebook it takes you to another page, ctrl-S and it will save to your downloads folder.

Variable definitions

Global Human Settlement Layer. Based on data from the GHSL project.

'ghsl_water_surface' - the fraction of land within 5km of the cluster that is classified as water surface
'ghsl_built_pre_1975' - the fraction of land within 5km of the cluster that is classified as built-up before 1975
'ghsl_built_1975_to_1990'
'ghsl_built_1990_to_2000',
'ghsl_built_2000_to_2014',
'ghsl_not_built_up' - land that was never built up
'ghsl_pop_density' - population density for the surrounding area (5km radius)
Landcover: based on the Copernicus Global Land Cover Layers (https://developers.google.com/earth-engine/datasets/catalog/COPERNICUS_Landcover_100m_Proba-V-C3_Global)

'Landcover_crops_fraction' - the fraction of land within 5km of the cluster that is classified as cropland
'landcover_urban_fraction' - the fraction of land within 5km of the cluster that is classified as urban
'Landcover_water_permanent_10km_fraction' - the fraction of land within 10km of the cluster that is classified as permanent water
'Landcover_water_seasonal_10km_fraction' - the fraction of land within 10km of the cluster that is classified as seasonal water
'Nighttime_lights' - a classic indicator of economic activity
'Dist_to_capital' - distance to the countries capital
'Dist_to_shoreline - distance to the nearest ocean shoreline
‘urban_or_rural’: Is the cluster in an urban (‘U’) or rural (‘R’) setting
