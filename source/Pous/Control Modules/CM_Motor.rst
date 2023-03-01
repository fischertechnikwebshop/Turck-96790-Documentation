.. _CM_Motor:

CM_Motor (pou)
==============


A control module to control a one direction fischerTechnik motor

-------------------------------------------------------------------------------------------



VAR_INPUT
~~~~~~~~~~

============  ======  =======  ============================================
Name          Type    Value    Comment                                       
============  ======  =======  ============================================
xStart        BOOL             Starts the motor                              
xStop         BOOL             Stops the motor                               
xStopAfter    BOOL             Stops the motor after ``tTimeVal`` seconds    
xSuspend      BOOL             Stops the motor while ``TRUE``                
============  ======  =======  ============================================

VAR_OUTPUT
~~~~~~~~~~~

========  ======  =======  =====================================================
Name      Type    Value    Comment                                                
========  ======  =======  =====================================================
xMotor    BOOL             Motor output                                           
**Status bits**
--------------------------------------------------------------------------------
xBusy     BOOL             Busy bits, indicates that motor (should be) running    
========  ======  =======  =====================================================

VAR RETAIN PERSISTENT
~~~~~~~~~~~~~~~~~~~~~~

==========  ======  =======  =========
Name        Type    Value    Comment    
==========  ======  =======  =========
tTimeVal    TIME    T#1S                
==========  ======  =======  =========

