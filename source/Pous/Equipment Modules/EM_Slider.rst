.. _EM_Slider:

EM_Slider (pou)
===============


.. image:: /_Graphics/EM_Slider.png
   :align: center
   :height: 400
   
-------------------------------------------------------------

Info
~~~~
The slider cannot be started if ``xReady == False``.

When started:

1.  The Slider will move forward
2.  After the slider has reached the pushbutton, the slider will change direction
3.  When the slider has reached the pushbutton in the back the ``xReady`` bit will be set to ``TRUE``

An error will be generated if the motor output is set to ``TRUE`` for more than 10 seconds. 


VAR_INPUT
~~~~~~~~~~

====================  ======  =======  ================================================
Name                  Type    Value    Comment                                           
====================  ======  =======  ================================================
xButtonSliderFront    BOOL             Button front input                                
xButtonSliderBack     BOOL             Button back input                                 
**Control bits**
---------------------------------------------------------------------------------------
xInit                 BOOL             Moves the slider to the home position             
xStart                BOOL             Starts the program loop                           
xSuspend              BOOL             Suspends the EM                                   
xTerminate            BOOL             Stops the equipment immediatly                    
xErrorReset           BOOL             Resets the Error latch                            
xInvert               BOOL             Inverts the motor direction if set to ``TRUE``    
====================  ======  =======  ================================================

VAR_OUTPUT
~~~~~~~~~~~

=================  ======  =======  =============================================================================
Name               Type    Value    Comment                                                                        
=================  ======  =======  =============================================================================
xSliderForward     BOOL             Motor direction forward output                                                 
xSliderBackward    BOOL             Motor direction backward output                                                
**Status bits**
-----------------------------------------------------------------------------------------------------------------
xReady             BOOL             Ready bit, indicating EM can be started                                        
xDone              BOOL             Done bit, indicating EM has finisched its loop (only ``TRUE`` for on cycle)    
xError             BOOL             Error bit, indicating an active error                                          
=================  ======  =======  =============================================================================

