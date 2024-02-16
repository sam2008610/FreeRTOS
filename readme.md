# EOS-Final 
This repository contains an extension of FreeRTOS, a popular real-time operating system for embedded devices, with support for Rate Monotonic Scheduling (RMS). RMS is a fixed-priority algorithm where the priority is determined based on the task's period; the shorter the period, the higher the priority. This scheduling policy is optimal for a set of periodic tasks.
- 2022 embedded operating systems final project
- 學生: 黃品程、曾柏翔
## Rate-monotonic on FreeRTOS​
- Implement Rate-monotonic scheduling policy on FreeRTOS
- Static priority and preemptive
- Tasks can execute periodically
- If the task misses deadline, it will be terminated
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
