# Simulate FCFS, CPU scheduling algorithm using queuing system

#include<stdio.h>;
#include<conio.h>;
void main()
{
clrscr();
int no_of_process,i;
float avarege_waiting_time=0,avarege_turnaround_time=0;
float waiting_time[10],process_exe_time[10],turnaround_time[10];
printf(&quot;Enter the no. of processes&quot;);
scanf(&quot;%d&quot;,&amp;no_of_process);
printf(&quot;Enter the execution time of all processes &quot;);
for(i=0;i&lt;no_of_process;i++)
{
scanf(&quot;%f&quot;,&amp;process_exe_time[i]);
}
turnaround_time[0]=process_exe_time[0];
for(i=0;i<no_of_process;i++)
{
turnaround_time[i+1]=turnaround_time[i]+process_exe_time[i+1];
// }
//for(i=0;i<no_of_process;i++)
waiting_time[i]=turnaround_time[i]-process_exe_time[i];
}
//for(i=0;i<no_of_process;i++)
	waiting_time[i]=turnaround_time[i]-process_exe_time[i];
}
printf("\n\n\n\nPROCESS\t\tTURNAROUND TIME\t\tWAITING TIME");

for(i=0;i<no_of_process;i++)
{
	printf("\n  %d \t\t %f \t\t%f",i+1,turnaround_time[i],waiting_time[i]);
	avarege_turnaround_time=avarege_turnaround_time+turnaround_time[i];
	avarege_waiting_time=avarege_waiting_time+waiting_time[i];
}
avarege_turnaround_time=avarege_turnaround_time/no_of_process;
avarege_waiting_time=avarege_waiting_time/no_of_process;
printf("\n\n AVAREGE \t%f\t\t%f ",avarege_turnaround_time,avarege_waiting_time);

//for(i=0;i<=no_of_process;i++)
//printf("the waiting time for all processes are");
getch();
}
