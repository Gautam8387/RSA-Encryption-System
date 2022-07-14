# RSA-Encryption-System

We have worked on RSA algorithm as a project.

First of all, our goal was to implement RSA from scratch.

*RSA_1.py contains the raw implementation of RSA without using any library. We used modular multiplication, modular exponentiation to deal with large numbers and we have created a package called bignumber with the program of operators: addition, substraction, multiplication and division. The package works on all arithmetic operations for the RSA_1.py. The program is working efficiently for 1024 bits and can be very easily extended upto 2048 bits and beyond.

Now, the idea was to explore the means to make RSA unique. In order to do that, instead of using bigmult to multiply two large numbers, we implemented fast polynomial multiplication with the help of FFT(Fast fourier transformation).

*In RSA_2.py, We simply extended what we have done in RSA_1 by including the FFT multiplication.

Then, we wanted to think of how we can practically use all the code that we have written. In order to do that, we explored the means of socket programming where we used RSA_1 and RSA_2 to secure a message sent over the a communication channel using socket where the client (sender) encrypt and the server (receiver) decrypt the message using the two programs (RSA_1 and RSA_2) of cryptography.


To Run the program, first run the file socket_server.py in terminal.
Then run any of the two files - socket_client_RSA_1.py or socket_client_RSA_2.py
Now type anything on client side and it'll be visible on the server.
