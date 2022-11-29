Shaghik Issakhani

CS 4310

11/26/22

                                                          FreeNOS Memory Process Manages
                                                                    
    FreeNOS is an operational system that controls primary memory and switches activities between primary memory and disk throughout execution. 
		
		FreeNOS maintains track of every memory location, independent of whether it is assigned to a process or is free. It determines how much memory 
		
		will be allotted to processes. It determines which processes acquire memory and when. It keeps track of when memory is released or unallocated 
		
		and changes the state accordingly. FreeNOS has a graphical setup interface that is browser-based. Multiple virtual machines may acquire storage 
		
		thanks to the built-in internet protocols. The FreeNOS plugin system allows you to enhance the built-in functionalities by adding third-party 
		
		applications. FreeNOS contains various dynamic memory problem fixes, as well as code and library design enhancements (libstd, libipc, libfs, liballoc).

		Furthermore, FreeNOS has expanded test coverage as well as the option to execute certain FreeNOS services and user apps on the host computer's 
		
		operating system. Finally, FreeNOS features a better heap scheduler, which improves overall system speed. This initial device is often referred 
		
		to as /dev/da0. FreeNOS-RELEASE (Yang et al. 120).iso should be replaced with the filename of the downloaded FreeNOS ISO file. Replace /dev/da0 with
		
		the identification number to read into.
		
		
		

    dd if=FreeNAS-RELEASE.iso of=/dev/da0 bs=64k  
  
6117+0 records in

6117+0 records out

400883712 bytes transferred in 88.706398 secs (4519220 bytes/sec)

     FreeNOS employs a technique of allocating memory dynamically. The technique of allocating memory space during operation or run time is known as 
     
     dynamic programming. Static memory allocation is only possible on the stack, but dynamic memory allocation is possible on both the stack and the heap.
     
     Recursion is an example of appropriate provisioning on the FreeNOS, where operations are placed on the call stack in sequence of appearance and 
     
     plucked off one by one when they reach the base case (Luna, Washington and Patricio 30). FreeNOS uses the Heap class to free memory, with the 
     
     delete[] operator.

int main()

{

   // Below variables are allocated memory
   
   // dynamically on heap.
   
   int *ptr1 = new int;
   
   int *ptr2 = new int[20];
 
 
   // Dynamically allocated memory is
   
   // deallocated
   
   delete ptr1;
   
   delete [] ptr2;
   
}
 
 

                                                                        Works cited 
                                                                          
Luna Encalada, Washington, Jonny Guaiña Yungán, and Patricio Moreno Costales. "Implementation of an Opensource Virtual Desktop Infrastructure System 

		Based    on Ovirt and Openuds." The International Conference on Advances in Emerging Trends and Technologies. Springer, Cham, 2020. 
		
	
Yang, Chiao-Tung, et al. "Implementation of Data Synchronization Mechanism in Virtual Desktop Infrastructure." International Journal of Informatics 

		and Information Systems 4.3 (2021): 157-167. 
