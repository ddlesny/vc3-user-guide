VC3 User Guide
==============
_Last revised: Monday, September 11, 2017_
questions/comments: lincolnb@uchicago.edu

### Table of Contents 
- [What is VC3?](#what-is-vc3-)
- [Getting Started with VC3](#getting-started-with-vc3)
  * [Prerequisites](#prerequisites)
  * [Bulding your first Virtual Cluster](#bulding-your-first-virtual-cluster)
        * [1. Login or Create Account](#1-login-or-create-account)
        * [2. Sign in to Globus](#2-sign-in-to-globus)
        * [3a. Login with your institutional ID](#3a-login-with-your-institutional-id)
        * [3b. Login with your Globus ID](#3b-login-with-your-globus-id)
        * [4. Complete or update your VC3 profile](#4-complete-or-update-your-vc3-profile)
        * [5. Connect an allocation](#5-connect-an-allocation)

# What is VC3?
Virtual Clusters for Community Computation, or VC3, is a platform for connecting clusters, grids, and clouds. VC3 can run overlay systems for a variety of cluster frameworks to make disparate resources appear as a single "virtual" resource for collaborative science. 

# Getting Started with VC3
## Prerequisites
In order to use VC3, you'll need an allocation or account with with a supported target resource. These include, but are not limited to:
  * _University of Chicago - Research Computing Center_
  * _University of Notre Dame - Center for Research Computing_
  * _Brookhaven National Laboratory - Scientific Data & Computing Center_
  * _Syracuse University - Research Computing_
  * _Texas Advanced Computing Center_
  * _NERSC_
  * _Amazon Web Services_
  * _Open Science Grid_
  * *and more!*

Institutions and resources are added frequently - be sure to subscribe to our newsletter and visit https://www.virtualclusters.org!

## Bulding your first Virtual Cluster

##### 1. Login or Create Account
When you first visit https://www-dev.virtualclusters.org, you'll be presented with a Login link in the top right of the screen. Click "Login" - this will take you to a Globus (https://globus.org) sign-in site. 

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_272.png?raw=true "VC3 Main Page")

##### 2. Sign in to Globus
You will then be asked to sign in with your institutional identity, or your Globus ID. If you are using the former, simply type in the name of your institution and click "Continue". Proceed to Step 3a.

Otherwise, click "Sign in with Globus ID" and proceed to the alternate Step 3b.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_273.png?raw=true "Sign-in")

##### 3a. Login with your institutional ID
You should be presented with a login page for your institutional ID, with your institution's branding. Go ahead and sign-in now. Note that your password is *not* sent to the VC3 or Globus web portals. Continue to step 4.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_275.png?raw=true "University Shibboleth page")

##### 3b. Login with your Globus ID
(_Alternative step - if you do not have an institutional ID supported by Globus_) 

<-- Globus ID page -->

##### 4. Complete or update your VC3 profile
Once you have signed in, you'll be asked to update or complete your VC3 profile with information such as your Institution and any other information we cannot directly extract from your Globus account. Click "Update Profile" once done.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_276.png?raw=true "Update profile")

##### 5. Connect an allocation 
After updating your profile, you can connect an allocation to the VC3 service. An allocation, in VC3, is defined as combination of a username and resource target that consumes some type of compute unit - regardless of whether it is billed as Service Units (many HPC centers), dollars (AWS, GCE), or priority (HTCondor and other opportunistic systems). 

Clicking *My Allocations* on the left shows all allocations currently associated with your account. You may select a new one by clicking *Connect Allocation*.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_277.png?raw=true "My allocations")

You will be able to select a resource target from the drop down menu, and enter an account name for the resource. This is the same account name that you use to SSH to the remote system.
![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_278.png?raw=true "Connect allocations")

Once you've connected your allocation, the system will validate it. 
![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_279.png?raw=true "List of allocations")

In order to create a virtual cluster, the VC3 software needs to be able to SSH to the remote resource. If you click your allocation, you should see a section titled *Public Token*.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_281.png?raw=true "pubtoken")

You will need to add this token to your Unix account, in the file `~/.ssh/authorized_keys`. You can either edit this file with your favorite editor (such as `nano`, `vim,` or `emacs`), or use the `echo` command to append it to the authorized keys file.

![alt text](https://github.com/vc3-project/vc3-user-guide/blob/master/images/screenshot_280.png?raw=true "Adding to the remote resource")
