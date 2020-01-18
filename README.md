# pingMachine
dumb threaded ping logger for some data gathering 
probs going to pull the log and split it out and cut out the failures and throw the IPs into a location API and see what kind of data set I can get


current version that is pushed to github is trash - speed tests tell me it will be done in like 33000 years. Gave it more threads and removed print - capped it off in the lab at 80% and we are now up to ~14k requests a second or something like that. It ruins my network speeds.... so I will likely need to find a way to level it off with out sacraficing speed. May take configuring.
