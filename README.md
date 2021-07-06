Threadcontrol

This a multithread controller for programs. It can process multiple instances of an command at once.


Usage: bash threadcontrol [--help || -h] [--multithread || -m] {threadcount} [--command || -c] {Parameters} [--tasks || -t] {tasks}

Note that when you enter conflicting parameters, the last one will be the one used. This means '-m 4 -m 8' will use 8 threads.

                [--help || -h]  :    Prints the help. If set, also prints help of $command
         [--multithread || -m]  :    Enables Multithreading. Default is set to 4 threads. Accepts value (eg. -m 8 equals to 8 threads)
                 {threadcount}  :    OPTIONAL: parameters passed to the command, seperated by spaces.

             [--command || -c]  :    Sets the command which should be executed
                     {command}  :    NESSESSARY: command to be executed
                  {Parameters}  :    OPTIONAL: parameters passed to the command, seperated by spaces.
                                :    -m 4 -tower -m 8 will pass -tower to the command. If you have parameters which do conflict with one of the above, they need to be add
                                :    ed to the command.
                                :    Instead of '-c command_which_uses_m_as_parameter -m Hello_World', you would need to enter '"-c command_which_uses_m_as_parameter -m H
                                :    ello_World"'

               [--tasks || -t]  :    Sets the tasklist by which threads are created. A task is passed as the last parameter to the command.
                                :    Every parameter passed between -c and -t will be treated as an commandparameter which will be passed to every thread. Every parameter
                                :     after -t will be a task, which will be passed to a single thread.
                       {tasks}  :    OPTIONAL: tasks to be worked on in a thread.
