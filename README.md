# MLD-Garbage-collector
gcc -g -c mld.c -o mld.o
gcc -g -c LinkedList/LinkedListApi.c -o LinkedList/LinkedListApi.o
gcc -g -c app.c -o app.o
gcc -g -o exe app.o LinkedList/LinkedListApi.o mld.o

Run the program as :
./exe


The program will print the leaked objects as below.
Program also print the structure db and object db, but here i am pasting the final
outcome of the program - set of leaked objects. As you can see, in app.c, I had intentionally leaked
the below object which is being shown as leaked.


Dumping Leaked Objects
-----------------------------------------------------------------------------------------------------|
0   ptr = 0x55cf26d86a40 | next = 0x55cf26d86a10 | units = 1    | struct_name = student_t  | is_root = FALSE |
-----------------------------------------------------------------------------------------------------|


