.. _EM_InputConveyer:

EM_InputConveyer (pou)
======================


.. image:: /_Graphics/EM_InputConveyer.png
   :align: center
   :height: 400
   
-------------------------------------------------------------

Info
~~~~
The conveyer cannot be started if ``xReady == False``.

When started:

1.  When the input sensor is activated the conveyer starts running
2.  After a piece has reached the output sensor, the conveyer will stop after X seconds
3.  When the conveyer has stopped the xReady bit will be (re)set to ``TRUE`` 

An error will be generated if the motor output is set to ``TRUE`` for more than 7 seconds. 
An error will also be generated if the output sensor is activated while EM is not active. 


VAR_INPUT
~~~~~~~~~~

===============  ======  =======  ================================
Name             Type    Value    Comment                           
===============  ======  =======  ================================
xInputSensor     BOOL             first sensor input                
xOutputSensor    BOOL             second sensor output              
**Control bits**
------------------------------------------------------------------
xStart           BOOL             Starts the program loop           
xStop            BOOL             Resets the operational latch      
xSuspend         BOOL             Suspends the EM                   
xTerminate       BOOL             Stops the equipment immediatly    
xErrorReset      BOOL             Resets the Error latch            
===============  ======  =======  ================================

VAR_OUTPUT
~~~~~~~~~~~

=================  ======  =======  =============================================================================
Name               Type    Value    Comment                                                                        
=================  ======  =======  =============================================================================
xMotor             BOOL             Conveyer motor output                                                          
**Status bits**
-----------------------------------------------------------------------------------------------------------------
xReady             BOOL             Ready bit, indicating EM can be started                                        
xReadyToReceive    BOOL             Ready to receice bit, indicating a piece may be placed at the EM               
xDone              BOOL             Done bit, indicating EM has finisched its loop (only ``TRUE`` for on cycle)    
xError             BOOL             Error bit, indicating an active error                                          
=================  ======  =======  =============================================================================

