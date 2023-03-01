.. _EM_OutputConveyer:

EM_OutputConveyer (pou)
=======================


.. image:: /_Graphics/EM_OutputConveyer.png
   :align: center
   :height: 400
   
-------------------------------------------------------------

Info
~~~~

This Module implements standard Status and Control bits.

The conveyer cannot be started if ``xReady == False``.

When started:

1.  The conveyer will run
2.  After a piece has reached the sensor, the belt will stop
3.  After a piece has been removed the ``xReady`` bit will be (re)set to ``TRUE``

an error will be generated if the motor output is set to ``TRUE`` for more than 10 seconds. 


VAR_INPUT
~~~~~~~~~~

=============  ======  =======  ================================
Name           Type    Value    Comment                           
=============  ======  =======  ================================
xSensor        BOOL             sensor input                      
**control bits**
----------------------------------------------------------------
xStart         BOOL             Starts the program loop           
xTerminate     BOOL             Stops the equipment immediatly    
xErrorReset    BOOL             Resets the Error latch            
=============  ======  =======  ================================

VAR_OUTPUT
~~~~~~~~~~~

========  ======  =======  =========================================
Name      Type    Value    Comment                                    
========  ======  =======  =========================================
xMotor    BOOL             Motor output                               
**Status bits**
--------------------------------------------------------------------
xReady    BOOL             Ready bit, indicating EM can be started    
xError    BOOL             Error bit, indicating an active error      
========  ======  =======  =========================================

