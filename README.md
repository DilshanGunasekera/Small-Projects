Small-Projects
==============

Contains small scale coding projects I work on during my free time.
-------------------------------------------------------------------------------------------------------------------------

1. Saturday, March 15th 2014

    Bloom Filter implementation


    I haven't uploaded anything on here before, so being my first project, I apologize for any git-hub oriented 
    formatting mistakes I make. 
    
    This works like a normal Bloom Filter, you choose the size when creating the object.
      I.e: filter = bloom_filter(6) #creates a 6 bit bloom filter object

    Bad input handling:
        filter = bloom_filter(8.5) #creates an 8 bit bloom filter object, the number is rounded down
        filter = bloom_filter(non-numeric-value) #uses object's integer method to convert to int, else error

    Hashing onto the filter:
        h4 = [h1 - 2 * h2 + h3]%field_length
        h1 is the standard division-remainder hashing function
        h2 is the standard middle square hashing function
        h3 is the standard folding hashing function (though the value is converted into length 4 first)

    Some implementation notes:
        - A bloom filter of 0 bits will always return False
--------------------------------------------------------------------------------------------------------------------------
