WELL44497ac
===========

WELL RNG 44497 a,c as described in http://www.iro.umontreal.ca/~panneton/WELLRNG.html.

The license can be found in at the top of the original code.

Exports
=======

init/1 - initializes and computes the first value of WELL
       - accepts:
            integer: for internal initial sample list
            list: externally generated sample list
       - returns {STATE,VALUE} (see well44497a:next/1)

next/1 - computes {STATE,VALUE} tuple
            STATE = {K: sample list, N: next seed index}
            VALUE: computed value for the given state
       - accepts tuple {K,N} (see above, only that N here
         is the current seed index)