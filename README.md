# Boost.EnanchedMap
A proposal to fix a design flaw into C++11/14 and boost's unordered_map

See profiling code:
https://github.com/Darelbi/PublicProfileTests/tree/master/BoostMemoryUsage

Or read related StackOverflow answer:
http://stackoverflow.com/a/30997235/1829943

Users of boost::unordered_map / std::unordered_map can incurr in excessive memory usage without
nothing documenting such behaviour. My proposal is to add a method that release manually
excessive memory usage (or alternatively document it better):


```
std::unordered_map<int,int> map;
add1000000Elements(map);
remove1000000Elements(map);
map.shrink(); // drops memory usage by few MBs to hundreds of MBs
```


