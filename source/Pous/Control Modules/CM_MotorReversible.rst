.. _CM_MotorReversible:

CM_MotorReversible (pou)
========================


A control module to control a two direction fischerTechnik motor

-------------------------------------------------------------------------------------------



VAR_INPUT
~~~~~~~~~~

===========  ======  =======  =============================================
Name         Type    Value    Comment                                        
===========  ======  =======  =============================================
xForward     BOOL             Starts the motor in the forwards direction     
xBackward    BOOL             Starts the motor in the backwards direction    
xStop        BOOL             Stops the motor                                
===========  ======  =======  =============================================

VAR_OUTPUT
~~~~~~~~~~~

================  ======  =======  =====================================================
Name              Type    Value    Comment                                                
================  ======  =======  =====================================================
xMotorForward     BOOL             Motor forwards output                                  
xMotorBackward    BOOL             Motor backwards output                                 
**Status bits**
----------------------------------------------------------------------------------------
xBusy             BOOL             Busy bits, indicates that motor (should be) running    
================  ======  =======  =====================================================

