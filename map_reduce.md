#   Mapper
*   Read single file at a time
*   Filter, transform, Interpretation
*   Key, Value pair after that
###   Shuffle Phase
*   First locally grouped by the key
*   A node is selected to process the same key data

#   Reducer
*   Do the sorting, aggregating the values per key
*   Write output to hdfs and then replicate
*   Bandwidth is low here as less shuffle across nodes
