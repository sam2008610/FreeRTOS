# EOS-Final 
## Rate-monotonic on FreeRTOS​
- Implement Rate-monotonic scheduling on FreeRTOS
- Static priority and preemptive
- Task can execute periodically
- If the task times out, it will be terminated
## API

```c
BaseType_t xTaskCreateTaskPeriod(	
    TaskFunction_t pxTaskCode,
	const char * const pcName,		
	const configSTACK_DEPTH_TYPE usStackDepth,
	void * const pvParameters,
	TaskHandle_t * const pxCreatedTask, 
	UBaseType_t PeriodTime
    );


xTaskCreateTaskPeriod(​

    Test_T_3, //TaskFunction_t​

    "P3",  //pcName​

    512,  //configSTACK_DEPTH_TYPE​

    NULL,  // pvParameters​

    NULL,  //TaskHandle_t​

    1000  //PeriodTime​

);
```