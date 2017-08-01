# FSGGC
A written framework (and example uses) to organize, classify, and specify geographic locales.

***FSGGC = Foley System of Global Geographic Classfication****

by Joseph Foley (github name Jodebane)

A framework for libraries of numerical and alphabetic variable assignments to specify places.
Each code is a classification for a geographic location, landmark, or system.

To get started, let's look at the basics: an example code is written below (with its numerical representation, followed by its alphanum representation [
 classifiers based on the main library (see example file for JSON format) ]).

THE SMITHSONIAN NATIONAL MUSEUM OF AMERICAN HISTORY COULD BE WRITTEN AS...

001-001-051:002-001-000:000.000.001

W-US-DC:IN-MU:1

World - United States - Washington DC : Indoor - Museum : 1

Before the first colon is the scope. It shows the territory for which the classification is relevant.
In the numerical system, each section must be of equal length. 
After the first colon is the classifier. It is a number, letter pair, or word that the library designates to mean 
	a type of place. In this example, an indoor tourist atraction can be written as 002 or 'IN'.

NOTE: Writing '000' means 'all', or can mean 'nothing in particular'. It is everything in the parent category, and it is nothing.

OR, IF WE WANTED TO RANK IT IN A LIST OF SAY, AS THE BEST MUSEUM IN A LIST OF THE TOP 100 BEST MUSEUMS
IN THE US, WHERE the number in the  WE COULD do this:

001-001-000:002-001-001:000.001.000

W-US:IN-MU-TOP:0.1 

The first two numbers in the scope are the same. But here's the difference: in the third layer of the scope, we have '000' meaning 'all'.
For the classifier, we don't just have '000' as the third. Instead, we have 001, as we have decided that it will be used to designate something
involving indoor museums that can be a subcategory if its own. 

The main point is that in the above, the 000s at the end of the first and last sections can be removed if we represent it in
a higher level notation. Why? They are irrelevant. The thing is, the position of the numbercode in the number classifier
must correlate with the same position in the scope section. If, after a certain point, 000 is all that remains in the classifier


MORE EXAMPLES: say we want another type of library, suppose, the entire solar system is layer 1 in scope, and layer 2 is the planet, numbered in order from the sun. 
Then say, for the classifier section, geogrpahic extremes can be category 1, and category 4 can be 'highest mountains'. In that place, number 1 for earth would be everest.

Everest = 001-003:001-004:000.001

Solar system - Earth : ExtremeElevations - Highest: [spaceholder], [rank on earth]

At layer 1, solar system = 001.
At layer 2, planets are numbered by order from the sun (001 = mercury, 002 = venus, 003 = earth..)

In classfications, at layer 1, 001 = extreme elevations

BASICALLY, THINK OF IT LIKE THIS:

Territory boundaries: Type of Place: Number of place


The framework of the system can be used to create any sort of set of
data, a library to represent any number of geographic classifications. In each one, there can be any number of layers and, letter-based codes can substitute a different number-based code. A place can have different code id's depending on the category. Category is the  variable that says what we are listing, and we can use any number of informational 'layers' to specify this.

Also, we can list more than one place. For instance, in the solar system classification above, we could instead have:

001-003:001-000:000.000

This would mean, all of the most extreme elevations on Earth. Extreme lowest point and extreme highest point would both be included in this, as the '000' means we are not specifying any particular subcategory after category 001. Anything with 000 does not stand out.

Now, for instance, 001-000:001-004:000.000

equals: highest points in the solar system. 

We can simplify this to:

001:001-004:000,

by removing the 0s from the first and last sections. Layer 2 is not relevant. 

JSON examples of libraries are listed elsewhere in the folder.
