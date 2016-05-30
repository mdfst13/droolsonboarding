# Requirements
We are working for a retail company that buys its products from different places in Asian mostly. each shop can go to the buying web site and say what he wants and put an order. 
Up to now, the transport cost was a estimated but not calculated on the content of the order. 
The purpose is to implement such a calculator.

## Data model

A customer puts an order that contains products. An order contains a lost of products with a number.
A product has 
* a name
* a height, 
* a witdh, 
* a depth, 
* transport type : if the product can be put with other products in a pallet, alone or bulk  (like sand for example)
* a weight

A product can be put on a pallet. a pallet 120 cm width and and 80 cm depth. It can be maximum 2 meters height and the weight should not exceed 1400 kg. We should use a simple algorithm to fill each pallet. It will be not optimized but we should used that as a margin of the costs.  a product that is bigger than 60 cm in width or depth or higher than 1m should be put alone in a pallet.

All products start from the same city and go to the same city in an order. A trip is composed f steps. Each step can be done by train, boat or truck.

| Transport| Cost 
| -- | -- | 
| boat | 0,2€/km |
| Train | 0,5€/km |
| Truck | 1€/km |

Here is the list of products in our test case
| Product | Transport type | Number | Height | Weight | depth | weight |
| -- | -- | -- | -- | -- | -- | -- |
| drill | pallet | 2:2 | 3:2 | 4:2 | 5:2 | 6:2 |
| screwdriver | pallet | 2:3 | 3:3 | 4:3 | 5:3 | 6:3 |
| Sand | bulk | 2:4 | 3:4 | 4:4 | 5:4 | 6:4 |
| Gravel | bulk | 2:5 | 3:5 | 4:5 | 5:5 | 6:5 |
| furniture | alone | 2:6 | 3:6 | 4:6 | 5:6 | 6:6 |