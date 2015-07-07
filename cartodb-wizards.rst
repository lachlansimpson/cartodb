==============================
CartoDB: Exploring the Wizards
==============================

In the `first tutorial <cartodb-first_steps.rst>`_ we quickly got up to the 
point where we could make a workable map with a few easy options and a data 
set. 

There are a number of popular ways to display data effectively on maps, and 
CartoDB comes with a handful out of the box. We will now explore some of the 
these wizards. 

Given the number of options available in some of these wizards, a *lot* of time
can be disappeared just playing around, testing. For this reason we recommend 
you spend time playing around outside of this class, in order to get the best 
result for your data. 

If you click on the Wizard's tab, you will see that in tutorial one we were 
working with the "simple" wizard.

Cluster Maps
============

Cluster maps are really good for showing data at various zoom levels. By 
clustering points that are in a similar vicinity and showing the total, it can
be easier to see where all the action is. 

As you zoom in and out, you will see the numbers increase as points move into
and out of the vicinity of each other.

.. image:: imgs/lobsters_as_clustermap.png


Choropleth Maps
===============

The Choropleth map allows for a second variable to be distinguished in the data - 
as you can see here the carapace length has been divided into five "buckets"
and each bucket given a colour. Now we can see a visualistation of the carapace
length on the map.

.. image:: imgs/choropleth_config.png

.. image:: imgs/lobsters_choroplethmap.png

If none of your variables can be divided into groups, this map is meaningless.  


Category Maps
=============

The category map is similar to the choropleth map but works better on distinct
data rather than continuous data.

In this instance, I've made a category map from the lobster's berried state - 
which is scientifical parlance for "with or without eggs". As the researcher 
Caleb Gardner from the University of Tasmania explains


    n=not berried (not carrying eggs beneath their tails).  y = berried.  All the other variants of berried state = y relate to the state of the eggs.  For example ye = berried eyed = the eyes of the larvae are visible as black dots inside the eggs.  These aren't recorded well so I'd reduce them all down to either y or n.

.. image:: imgs/lobster_categorymap.png


Bubble Maps
===========

Bubble maps are useful for visualising size differences of a numerical value 
column in your data. In the lobster's case, we can again see the carapace
length used, and the different sized bubbles as a result. Note also how it 
stacks neatly the lobsters of different length that aere found in the same 
spot.

.. image:: imgs/lobster_bubblemap.png




==============
END tutorial 2 
==============




