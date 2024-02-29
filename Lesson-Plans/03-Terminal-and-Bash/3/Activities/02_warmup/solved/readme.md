## Solution Guide: Warm-up


- The first step is to navigate into the `/03-student/day3/warmup` folder on your virtual machine. To do this, run the following commands:

   - `cd /03-student/day3/`

   - `cd warmup`

- Create a folder called `subpoena_request`:

  - `mkdir subpoena_request`

- Next, find the files dated 0719. Run the following command:   

  - `find -type f -iname *0719*`

     This will return the following two files:

       ```
       ./WEBACCESS/0719Apache
       ./WEBACCESS/IIS_0719
       ```

- Move the files into the `subpoena_request` folder using a wildcard:

  - `mv ./WEBACCESS/*0719* ./subpoena_request/`

 - Find the phone records that provide proof of calls made to Sugar's number,  454-555-3894, and place them in a file called `Calls_to_Sugar`:

   - `grep 454-555-3894 ./PHONE_LOGS/* > Calls_to_Sugar`

- Move the file into the `subpoena_request` folder:

  - `mv Calls_to_Sugar ./subpoena_request/`

**Bonus**

- The following three incoming phone numbers are in the file we created called `Calls_to_Sugar`:

  - 212-555-2732

  - 212-555-2733

  - 212-555-2734

- To look up the owners of these three phone numbers, run the following:

  -  `grep '212-555-2732\|212-555-2733\|212-555-2734' ./DIRECTORIES/*`

- The results show the following:

    - 212-555-2734    Mr Goodbar  

    - 212-555-2732    Ruth  

    - 212-555-2733    Henry

  It looks like Mr Goodbar has also been in contact with Sugar.      

---

&copy; 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
