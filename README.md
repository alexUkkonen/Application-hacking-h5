# Application-hacking-h5

## a) 

I wasn't present during the lesson so i don't know what methods where used in lab0.

First i started by using `$strings gcd_example1`. This tells me if there are any low hanging fruits. the file isn't that big so i can look trough it manualy.

The next thing i did was run the file. Our issue is the segmentation fault.

<img width="654" height="85" alt="image" src="https://github.com/user-attachments/assets/e2a9e01a-e4c8-43dd-93ce-794a4b23166d" />

I wasn't sure if i was allowed to but i didn't know how to solve this without doing it so i opened the .c file.

<img width="617" height="565" alt="image" src="https://github.com/user-attachments/assets/f9d525b4-9a93-4fdd-b336-df31c4272178" />

When we look at the code we can see that since bad_message == NULL the program is trying to print to 0 wich it doesn't have permission to. we fixed this by exiting the code with an error message if this happens.

<img width="829" height="691" alt="image" src="https://github.com/user-attachments/assets/923bcc8e-7f2b-4ea5-8bec-a0116346f72d" />

Now we compile the file and try! It's fixed.

<img width="874" height="199" alt="image" src="https://github.com/user-attachments/assets/95626cc3-8137-497a-aff3-04ee20eeccde" />

## b)

First we read the readme.

The next thing i did was run `$ strings passtr`. thiss tells us the flag emmediately.

<img width="1034" height="498" alt="image" src="https://github.com/user-attachments/assets/cd640b2e-a48e-483b-b3e2-c31daec863c8" />

## c)

First we read the README.md The file tells us not to read the sourcecode and to use the make and where commands.

We run the program, it tells us it needs and argument so we run it with a "random" argument. this returns 1.

<img width="871" height="157" alt="image" src="https://github.com/user-attachments/assets/4fa885cf-cd6e-4b0e-b409-f00e772c7d82" />

Next we use strings to check what we can se.

<img width="894" height="1170" alt="image" src="https://github.com/user-attachments/assets/e9d909aa-73a3-43de-b326-06da66b96f7d" />

We notice that strcmp is missing but we have strlen. this means that the program only cares about length of the password.

we use ltrace to see the program run in real time.

<img width="1617" height="124" alt="image" src="https://github.com/user-attachments/assets/09cde6c0-4843-42d3-9d11-519387094ce9" />
