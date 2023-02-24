# neuropace
pacman ieeg analysis prep for RNS data


### Prep Behavioral Data

Instead of converting the jsons to a csv as we do in the normal pipeline, I need to stitch the jsons together since a modified version of the task with only 20 trials is run 12 times, rather than the normal 240 trials version run with blocks. Thus, we need to copy all json files to the raw folder in the data dir and then run the neuropace parser from the data_parser repo.

Next, we get the start and stop times for each trial using the `<sub_name>.Rmd` script in the `behavior` folder. We will use the outputted csv, `data/<sub_name>_runX_triggers.csv` to try to match up with the triggers around blocks in the RNS data.  
