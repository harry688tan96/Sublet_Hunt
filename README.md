# Sublet Hunt 

## A project that crawled all sublet advertisements in Kijiji, and extracted sublet sale posts in Facebook. 
#### Facebook sublet sale groups are widely used by the students from the University of Waterloo, Laurier University and Connestoga College in searching for 4-month sublets in Waterloo region. Kijiji comes in second. <br> Among a list of sublet sale groups that are available in Facebook, the following groups which have the most members are selected for data extraction:
  * [**Student Housing in Waterloo**](https://www.facebook.com/groups/110354088989367/)
  * [**UW/WLU 4 Month Subletting**](https://www.facebook.com/groups/WaterlooSublet/)
  * [**Housing**](https://www.facebook.com/groups/UWhousing/)
------
### Reason for this project:
> * Facebook is a great place for people to search for sale items. However, there are some drawbacks with these sale posts. There are currently no filters (ie. price or location region) that allow the users to sort out the sale posts. <br> Besides, all of the buyers and sellers' sale posts are aggregated together, so buyers might encounter trouble in searching for sale posts that he/she is interested in, and sellers might have trouble to look for potential buyers within the aggregated posts.
> * This project primarily aims to implement simple filters on the sublet sale posts in Facebook for quick search. 
> * Since some students post sublet advertisement in Kijiji, I combined the data extracted from the Facebook sale groups with the data crawled from Kijiji. Then, I applied filters on these sublet advertisements for sublet comparisons.
------
### Highlight of each of the Jupyter Notebooks in this project:
* [**Streets-in-Waterloo-Ontario.ipynb**](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Streets-in-Waterloo-Ontario.ipynb)
  - Calculates the distance between the streets in Waterloo and the location of the University of Waterloo using **Geopy** library
  - The result of this notebook is used in the [Facebook Housing Sublet.ipynb](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Facebook%20Housing%20Sublet.ipynb) mentioned below
* [**Facebook Housing Sublet.ipynb**](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Facebook%20Housing%20Sublet.ipynb)
  - Extracts sublet sale posts from the Facebook sublet group mentioned above using **Facebook Graph API**
  - Implemented **regex** using the street names in Waterloo as regex pattern (A list of street names in Waterloo can be found in [*Geographic.org/streetview*](https://geographic.org/streetview/canada/on/city_of_waterloo.html))
  - Implemented filters such as **price of the item**, **location of the sale posts** and **popularity of the item**. The **popularity** of an item is measured based on the number of comments in that item post
  - Google Map widget is included in the notebook for the purpose of understanding which locations are highly favoured by the sublet buyers
* [**Kijiji Web Scraping.ipynb**](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Kijiji%20Web%20Scraping.ipynb)
  - Web Crawled the sublet advertisements available in [Kijiji](https://www.kijiji.ca/b-kitchener-waterloo/room-rental-roommate/k0l1700212) using **BeautifulSoup**
* [**Ideal_sublet_room.ipynb**](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Ideal_sublet_room.ipynb)
  - Combined the data collected from [*Facebook Housing Sublet.ipynb*](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Facebook%20Housing%20Sublet.ipynb) and [*Kijiji Web Scraping.ipynb*](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/blob/master/Kijiji%20Web%20Scraping.ipynb) for users search

***\* Multiprocessing is used in the first three notebooks to maximize concurrency that speeds up computation.***
### Note
 For better view of the Jupyter Notebook in GitHub, you might consider using [Jupyter nbviewer](http://nbviewer.jupyter.org/) to render the output of the notebook. For simplicty, [click](http://nbviewer.jupyter.org/github/harry688tan96/Sublet_Hunt/tree/master/) to view all of my Jupyter Notebooks that are already rendered! :smile:
 
