Header required: #include <fstream>



Three class for excuating file:



ifstream    : class for reading input data from file

	ifstream <valuable\_name> (<"directory">)



ofstream    : class for writing data into file

	like ifstream



fstream     : class for writing \& reading





				MODE

ios::in     : input activities (normal mode of ifstream)



ios::out    : output activities (normal mode of ofstream)



ios::binary : use for binary file



ios::ate    : set the file pointer to the end of the file when file is opened



ios::app    : if file has data inside, then new data will insert in the end



ios::trunc  : when write data into file, old data will be erased

	<class_file> <valuable_name>(<"directory">, [mode])

	or   <valuable_name>.open(<"directory">,[mode])





	#NOTE: CAN USE PIPE (|) for combine more modes



	#NOTE: IN DIRECTORY, USING (\\\\) INSTEAD OF (\\)





			READING & WRITING (TEXT)

<file_name> << <valuable_name>        : writing data from value into file



<file_name> >> <valuable_name>        : reading data from file into value (stop if get " ") 



getline(<file_name>, <valuable_name>) : reading data from file into value (stop if get "\n")





