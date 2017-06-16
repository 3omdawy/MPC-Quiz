
# MPC-Quiz
Environment for CppAd and Ipopt on Windows

I can't remember the actual steps but roughly I downloaded CppAd and IpOpt files, built them (especially CppAd to add configure.hpp) and added them to the project. Refer to the instructions using Docker in the project readme.
Then it was a matter of finding online the dlls that corrected linking errors (mainly IpOpt and mcvsr100)
The part of linking with Python in matplotlib did not work with me so I commented it out, but otherwise it build and works with VS2017 (verified values using debugging).
Note: Ipopt files (dlls, lib ...) are for Windows 10 64-bit.
If you have a 32-bit operating system may be you should search for IpOpt dlls for 32-bit systems.
bad_alloc exception is related to msvcp100.dll, msvcr100.dll , and msvcr100d.dll.
Do you include them in your directory? May be you need to include the right dlls if your system is different fro mine.
Note: I also needed to comment the line containing Integer print_level and max_cpu_time.
For all details: https://discussions.udacity.com/t/mpc-project-on-windows/249654/18
