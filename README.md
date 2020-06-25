# mdl_grade_category
Add an exception before an infinite loop is entered in lib/grade/grade_category.php

For a variety of reasons, a disjointed relationship can occur between {grade_items} and {grade_categories}. When this occurs and when a user views the gradebook, the code enters an infinite loop.  This soft fix identifies the scenario where the code would enter an infinite loop, but throws an exception to prevent it.  It also prevents another error, although not an infite loop, many identical categories in {grade_items} is not desireable in our code base.

You can use whichever message you like in lang/en/error.php, but we opted to use one already there, and to add another one.  I hope this helps.
