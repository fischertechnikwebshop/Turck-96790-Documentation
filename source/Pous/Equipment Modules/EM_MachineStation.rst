.. _EM_MachineStation:

EM_MachineStation (pou)
=======================


.. image:: /_Graphics/EM_MachineStation.png
   :align: center
   :height: 400
   
-------------------------------------------------------------

Info
~~~~
The conveyer cannot be started if ``xReady == False``.

When started:

1.  The conveyer will run
2.  After a piece has reached the sensor, the belt will stop and the machine motor will run for X seconds
3.  After the machine motor has finished the conveyer will run for X seconds
4.  When the timer is DONE the xReady bit will be (re)set to ``TRUE`` 

An error will be generated if the motor output is set to ``TRUE`` for more than 7 seconds. 
An error will also be generated if the sensor is activated while EM is not active. 


VAR_INPUT
~~~~~~~~~~

=============  ======  =======  ================================
Name           Type    Value    Comment                           
=============  ======  =======  ================================
xSensor        BOOL             Sensor input                      
**Control bits**
----------------------------------------------------------------
xStart         BOOL             Starts the program loop           
xSuspend       BOOL             Suspends the EM                   
xTerminate     BOOL             Stops the equipment immediatly    
xErrorReset    BOOL             Resets the Error latch            
=============  ======  =======  ================================

VAR_OUTPUT
~~~~~~~~~~~

================  ======  =======  =============================================================================
Name              Type    Value    Comment                                                                        
================  ======  =======  =============================================================================
xMachineMotor     BOOL             Machine motor output                                                           
xConveyerMotor    BOOL             Conveyer motor output                                                          
**Status bits**
----------------------------------------------------------------------------------------------------------------
xReady            BOOL             Ready bit, indicating EM can be started                                        
xDone             BOOL             Done bit, indicating EM has finisched its loop (only ``TRUE`` for on cycle)    
xError            BOOL             Error bit, indicating an active error                                          
================  ======  =======  =============================================================================

