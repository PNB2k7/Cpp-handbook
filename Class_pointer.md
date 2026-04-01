    		Pointer's Objects	



    Declaration:

<class\_name> \*<object\_ptr\_name>;



    Memory Allocation

<object\_ptr\_name> = new <class\_name>(\[Arguments]);



Notes:

* Arguments have to match with one constructor
* Using constructor has no parameters, we still must use "()" within using new



    Using Pointer

  If don't use "new", pointer can point to the address of an existing object

<object\_ptr\_name> = \&<object>;



  When access to member of pointer object

<object\_ptr\_name> -> <member>(\[Arguments]); //Arguments with a method



    Free Pointer

delete <object\_ptr\_name>; //Only use when pointer have memory allocation by "new"



    		Arrays Objects 

  Static List Objects

<class\_name> <list\_name>\[<Quantity>];



Notes:

* Can ignore quantity when don't know exactly number;
* Need constructor has no parameters or implicit value of parameters



  Dynamic List Object

<class\_name> \*<list\_name> = new <class\_name>\[<Quantity>];



//Freeing memory - Like dynamic arrays



    Using list

<list\_name>\[<index>].<member>(\[Arguments]);



