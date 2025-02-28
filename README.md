# arma-3-life-cation-core

This is the cationstudio core system for ArmA 3 RPG Life

<a href="https://www.buymeacoffee.com/julianbauer" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-red.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>

## Installation

A working installation of ArmA Life RPG Framework is required for a successful installation. Modifying the ArmA Life RPG Framework could cause errors – feel free to connect to our discord if you have a problem.

### Step 1

Download the newest release and extract the archive.

### Step 2

Copy the folder “cation” in your root folder (subsequently called \<mission\>) of your mission.

### Step 3

Open \<mission\>/description.ext and insert under class CfgFunctions {

`#include "cation\cation_functions.cpp"`

**Example:**

```
class CfgFunctions {
    #include "cation\cation_functions.cpp"
    #include "Functions.hpp"
};
```

### Step 4

Go to the bottom of \<mission\>/description.ext, insert

`#include "cation\cation_master.cpp"`

and save the file.

### Step 5

Open \<mission\>/CfgRemoteExec.hpp (if it doesn’t exist then skip this setp.)

Search the following section

```
class Functions {
    mode = 1;
    jip = 0;
```

and insert below

`#include "cation\cation_remoteExec.cpp"`

and save the file.

**Example:**

```
class CfgRemoteExec {
    class Functions {
        mode = 1;
        jip = 0;

        #include "cation\cation_remoteExec.cpp"
 
        /* Client only functions */
```

**That's it!**

You have installed the cationstudio core system successfully!
