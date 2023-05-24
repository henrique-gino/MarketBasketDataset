9# MarketBasketDataset

We use a public available dataset, published by dunnhumby and x university and hosted in 'link'.

In the 'data' folder we need to have three datasets to create the final market basket network dataset: 'hh_demographic', 'product', 'transaction_data'.

These are the steps executed in the 'network_dataset_creation' notebook:
1. pass
2. etc.



# Temporal Networks

* The three available temporal networks are: 'Low-income network.dat', 'Middle-income network.dat', and 'High-income network.dat'.

The format of the network file is: "node_1_id"  "node_2_id"  "timestamp", where each line correspond at an edge between node_1 and node_2 in a specific timestamp.

* The metadata information of the networks are available at: 'Products price range.txt'.

The format of the metadata information is: "node_id"   "price_range", varying between 0 (Very low), 1 (Low), 2 (Normal), 3 (High), and 4 (Very High).

Network sizes:

Networks                Nodes          Edges          Timestamps
Low-income network      9,450          387,031        346 (days)           
Middle-income network   9,859          470,224        346 (days)           
High-income network     3,071          46,410         346 (days)    
