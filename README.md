#include “xparameters.h”
#include “xgpio.h”
#include “xutil.h”

//====================================================

int main （void) 
{

   XGpio dip、push;
   int i、psb_check dip_check;

   xil_printf（“-- 程序启动 --\r\n”);

   XGpio_Initialize（&dip， XPAR_DIP_DEVICE_ID）; Modify this （修改此项）
   XGpio_SetDataDirection（&dip， 1， 0xffffffff);

   XGpio_Initialize（&push， XPAR_PUSH_DEVICE_ID）; Modify this （修改此项）
   XGpio_SetDataDirection（&push， 1， 0xffffffff);


   而 （1)
   {
	  psb_check = XGpio_DiscreteRead（&push， 1);
	  xil_printf（“按钮状态 %x\r\n”， psb_check);
	  dip_check = XGpio_DiscreteRead（&dip， 1);
	  xil_printf（“DIP 开关状态 %x\r\n”， dip_check);

	  LED_ip设备上的 Output DIP 开关值

	  for （i=0;i<9999999;我++);
   }
}
