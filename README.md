# MarketBasketDataset

This repository exposes and explains the creation of the "Market Basket Dataset", which was used in the paper "Exploratory Analysis on Market Basket Data using Network Visualization" as a network of products bought in groceries stores. 

We use a publicly available dataset named "The Complete Journey", published by dunnhumby and hosted in [this link](https://www.dunnhumby.com/source-files/). The dataset contains household-level transactions over two years from a group of 2,500 households who are frequent shoppers at a retailer. These transactions are all of a household’s purchases within the store, not just those from a limited number of categories. Also, the dataset includes demographics and direct marketing contact history for select households.

To create the "Market Basket Dataset", you will need only three files from "The Complete Journey": *hh_demographic*, *product*, *transaction_data*.

These are the steps executed in the 'network_dataset_creation' notebook:
1. Create demographic classes for households (annual income, has kids, age);
2. Filter unimportant items for the analysis (such as gas/oil, or even items from undesired departments), then create a price class for all items, based on the quantiles of the product price distribution;
3. Create the product metadata dataframe (with ID, taxonomy, price class and department);
4. Create the interactions dataframe, by combining all products bought together in the same basket and removing the duplicates (as in ProductA <-> ProductB, ProductB <-> Product A);
5. Update the interactions dataframe with new product ids for all products (necessary for adequate input in LargeNetVis);
6. Update the product metadata dataframe with the new ids.


# Temporal Networks

* The three available temporal networks are: 'Low-income network.dat', 'Middle-income network.dat', and 'High-income network.dat'.

The format of the network file is: "node_1_id"  "node_2_id"  "timestamp", where each line correspond at an edge between node_1 and node_2 in a specific timestamp.

* The metadata information of the networks are available at: 'Products price range.txt'.

The format of the metadata information is: "node_id"   "price_range", varying between 0 (Very low), 1 (Low), 2 (Normal), 3 (High), and 4 (Very High).

Network sizes:


| Networks              | Nodes      | Edges    | Timestamps |
| -------               | ---        | ---      | ---        |
| Low-income network    | 9,450      | 387,031  | 346 (days) |
| Middle-income network | 9,859      | 470,224  | 346 (days) |      
| High-income network   | 3,071      | 46,410   | 346 (days) |
