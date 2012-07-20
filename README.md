WELL44497ac
===========

WELL RNG 44497 a,c as described in http://www.iro.umontreal.ca/~panneton/WELLRNG.html.

The license can be found in at the top of the original code.

Exports
=======

init/1 - initializes and computes the first value of WELL<br/>
       - accepts:<br/>
            integer: for internal initial sample list<br/>
            list: externally generated sample list<br/>
       - returns {STATE,VALUE} (see well44497a:next/1)<br/>

next/1 - computes {STATE,VALUE} tuple<br/>
            STATE = {K: sample list, N: next seed index}<br/>
            VALUE: computed value for the given state<br/>
       - accepts tuple {K,N} (see above, only that N here<br/>
         is the current seed index)