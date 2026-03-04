Header required: #include <fstream>



Three class for excuating file:



* ifstream    : class for reading input data from file

&nbsp;	ifstream <valuable\_name> (<"directory">)



* ofstream    : class for writing data into file

&nbsp;	like ifstream



* fstream     : class for writing \& reading





&nbsp;			MODE

* ios::in     : input activities (normal mode of ifstream)



* ios::out    : output activities (normal mode of ofstream)



* ios::binary : use for binary file



* ios::ate    : set the file pointer to the end of the file when file is opened



* ios::app    : if file has data inside, then new data will insert in the end



* ios::trunc  : when write data into file, old data will be erased

&nbsp;	<class\_file> <valuable\_name>(<"directory">, \[mode])

&nbsp;  or   <valuable\_name>.open(<"directory">,\[mode])





&nbsp;	#NOTE: CAN USE PIPE (|) for combine more modes



&nbsp;	#NOTE: IN DIRECTORY, USING (\\\\) INSTEAD OF (\\)





&nbsp;			READING \& WRITING (TEXT)

* <file\_name> << <valuable\_name>        : writing data from value into file



* <file\_name> >> <valuable\_name>        : reading data from file into value (stop if get " ") 



* getline(<file\_name>, <valuable\_name>) : reading data from file into value (stop if get "\\n")





