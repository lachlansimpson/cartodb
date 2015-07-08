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
stacks neatly the lobsters of different length that are found in the same 
spot.

.. image:: imgs/lobster_bubblemap.png


It's not a perfect data set to show this information - a common usage is as a
population bubble for towns on a map, or as in this case, medal tally in the 
Olympics

.. image:: https://visualign.files.wordpress.com/2012/08/2012londonresults.png


Torque Maps
===========

Torque maps change on a variable that shows either regular growth or a date 
format. For example, if you have a date value that changes per tuple (eg: year 
in which a national constitution is written), your map can automatically show
this in motion. 

Below we see the that the lobster data automatically picks up the tuple id as a
variable to torque, so you see each dot appearing in order. This isn't really 
very usful in this case but shows how the Torque map works.

.. image:: imgs/recorded.gif

The Torque map has some interesting properties, so let's spend some time 
playing.

First, as noted above, the id number is a valid torque, but somewhat useless. 
Let's take a look at the underlying data and see if there is a better field to 
use.

At the top of the screen, you will see the view button, select "Data View" and
we will see the underlying data.

.. image:: imgs/cartodb_view.png

If we scroll across to the shot_date field, we see that the dates are there, 
but unrecognised - they are listed as "string".

.. image:: imgs/cartodb_data_types.png

Drop down the arrow and choose "Change data type..."

.. images:: imgs/cartodb_data_change.png

You will then be shown the types of data that are available. Choose date.

.. images:: imgs/cartodb_data_choice.png

And then you get a warning. Ergh. Unconvertible data will be lost? What does 
that mean - is it just a warning or is it specifically a warning based on *our*
data? Ergh. Coders need to spend more time with users. Let's click Yes and see
what happens.

.. images:: imgs/cartodb_data_warning.png

And now we see that large parts of the column are null. Bugger. American date
fascists.

**bugger**.

Right. Since we are footloose and fancyfree, let's just fix the data and load 
it again. (



==============
END tutorial 2 
==============




