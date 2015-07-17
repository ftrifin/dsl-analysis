# How to Use #

  * [Instance analysis](HowToUse#Instance_Analysis.md)
  * [Relationship analysis](HowToUse#Relationship_Analysis.md)
  * [Clone analysis](HowToUse#Clone_Analysis.md)

[Non-Xtext-based EMF Models](HowToUse#Non-Xtext-based_EMF_Models.md)

_Note: some of the screen shots below come from using the [Geppetto](https://github.com/cloudsmith/geppetto/wiki) for the [Puppet](http://docs.puppetlabs.com/learning/) language with the DSL Analysis tool._

## Instance Analysis ##

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif)

1. Select "DSL Analysis" > "Metamodel elements" > "Count" to open the following window.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_count.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_count.gif)

2. Select all projects that will be included in the analysis. Also, enter the file extension for the Xtext-based DSL.

3. Click "Finish." After processing, a "Metamodel Element Totals" view will be displayed similar to the following view.

This view displays the number of times each element is used ("All count") and the number of models at least one occurrence of the element is found in ("Model count").

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_count.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_count.gif)

The data can be downloaded as a comma-delimited file by clicking on the menu button for the view (i.e., down arrow to the right of the view) and selecting "Save to file."

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_options_2.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_options_2.gif)

## Relationship Analysis ##

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif)

1. Select "DSL Analysis" > "Metamodel elements" > "Cluster" to open the following window.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_count.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_count.gif)

2. Select all projects that will be included in the analysis. Also, enter the file extension for the Xtext-based DSL.

3. Click "Next," and a window similar to the following window will appear.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_cluster.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_cluster.gif)

4. Select all metamodel elements that will be included in the clustering process. Also, enter the number of clusters to generate and the link type to compare the distance values of the elements. The "Complete" link type is selected as default.

5. Click "Finish." After processing, a "Metamodel Element Clusters" view will be displayed similar to the following view.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_cluster.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_cluster.gif)

The associated [dendrogram](http://en.wikipedia.org/wiki/Dendrogram) of the clusters can be obtained by either copying or saving the dendrogram in [Newick format](http://en.wikipedia.org/wiki/Newick_format) for a cluster. The format can then be exported to a tree generator web site such as http://www.trex.uqam.ca/index.php?action=newick&project=trex.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_newick.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_newick.gif)

Several types of data can be downloaded by clicking on the menu button for the view (i.e., down arrow to the right of the view).

  * _Co-occurrence Stats_ &ndash; Comma-delimited file of the co-occurrence of metamodel elements in the observed models.
  * _Distance matrix_ &ndash; Distance matrix of metamodel elements based on co-occurrence data in two formats: comma-delimited file and [Weka](http://www.cs.waikato.ac.nz/ml/weka/) ARFF file.
  * _Clusters_ &ndash; Summary of generated clusters including Newick formatted dendrograms.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_options.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_options.gif)

## Clone Analysis ##

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_options.gif)

1. Select "DSL Analysis" > "Detect Clones" to open the following window.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_clone.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_clone.gif)

2. Selecting projects and entering the file extension for the DSL instances is the same as before. The additional configuration settings are the minimum node size and type of clone detection.

  * _Minimum Node Size_ &ndash; limits the size of the sequence of nodes that will be included in the detection process
  * _Detection Type_ &ndash; determines whether exact matching clones or parameterized clones (i.e., that can vary in the naming used) will be detected

3. Click "Finish." After the detection process, a "Clone Detection" view will be displayed similar to the following view.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_clone.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_view_clone.gif)

4. Clone groups containing clones representing the same duplication will be displayed. Double clicking on the individual clones will open the code associated with the clone highlighted in the source editor.

## Non-Xtext-based EMF Models ##

EMF models not associated with an Xtext-based DSL can utilize the instance and relationship analyses, but not clone analysis.

If the models do not have a valid nsURI, the metamodel must be selected by clicking on "Include metamodel" and browsing for the metamodel to be included.

![https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_metamodel.gif](https://svn.codespot.com/a/eclipselabs.org/dsl-analysis/wiki/dslanalysis_wizard_metamodel.gif)