# Boost.EnanchedMap
A proposal to fix a design flaw into C++11/14 and boost's unordered_map

See profiling code:
https://github.com/Darelbi/PublicProfileTests/tree/master/BoostMemoryUsage

Or read related StackOverflow answer:
http://stackoverflow.com/a/30997235/1829943

Basically, there's a "undocumented" behaviour that needs to be documented, a nice alternative is to provide an alternative method to allow "disposing" of unneeded memory manually
