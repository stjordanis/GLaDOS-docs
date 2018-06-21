# New Web Interface

We have developed a new [web interface](https://www.ebi.ac.uk/chembl/beta/) that will eventually replace the [current one](https://www.ebi.ac.uk/chembl/) completely. It is still in a beta stage, this means that it provides all the mayor features, but it is expected to have some known and unknown bugs. We will be working on fixing them as a next stage.

## New Features

### Free Text Search

* The bar will provide some suggestions as you write. 
* You don't need to click on a different button to search for different entity types \(Compounds, Targets, Assays, Documents, Cells or Tissues\) anymore , the interface will search among all entities for you. 
* The search bar now appears in all the pages, including report cards, so you don't have to go back to the main page to search for another term. 
* Our new interface uses elasticsearch indexes, you can use a DSL to build complex queries, see our [guide](searching-guide.md). 

### Structure Search

* You can search by using the [Marvin JS sketcher](https://chemaxon.com/products/marvin-js). You can open it just by clicking on the "structure" icon on the search bar:

![](.gitbook/assets/screen-shot-2018-06-20-at-17.06.11.png)

* For the substructure and similarity results we have now included structure highlighting on the results. the highlight can be turned on or off. See for example: [https://www.ebi.ac.uk/chembl/beta/g/tiny/O/X4tGAntE5huqwzOIcrlg==](https://www.ebi.ac.uk/chembl/beta/g/tiny/O/X4tGAntE5huqwzOIcrlg==) 

### Filters

For the search results and other results that you can produce in the interface there are filters available at the left side of the page:

<img src="https://github.com/chembl/GLaDOS-docs/raw/master/.gitbook/assets/screen-shot-2018-06-21-at-12.39.37.png" width="350" height="400">
[https://www.ebi.ac.uk/chembl/beta/g/\#browse/compounds](https://www.ebi.ac.uk/chembl/beta/g/\#browse/compounds)

With these filters you can easily see the distribution of the data. The sizes of the rectangles behind each value represent the proportion of items with that value for that property in the data. You can also click on the filter the data. 

By clicking on the "settings" button

![](.gitbook/assets/screen-shot-2018-06-21-at-13.35.17.png)

You can open a menu to configure the filters panel

![](.gitbook/assets/screen-shot-2018-06-21-at-13.36.42.png)











