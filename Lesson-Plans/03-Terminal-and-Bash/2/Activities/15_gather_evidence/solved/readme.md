## Solution Guide: Gather Evidence

- The first step is to navigate into the `/03-student/day2/Gathering_Evidence/` folder on your virtual machine. To do this, run the following command:

   - `cd /03-student/day2/Gathering_Evidence/`
       
- In the `Gathering_Evidence` folder, make a directory called `Sugar_evidence` by running:   

  - `mkdir Sugar_evidence`
         
- Next, move into the email directory:

  - `cd email`
      
- List the emails referencing Sugar, and place the results in a file called `Sugar_email_evidence`: 
        
  - `grep -il sugar * > sugar_email_evidence`
         
- Next, add to the same file the number of emails that contain Sugar:
    
  -  `grep -il sugar * | wc -l >> sugar_email_evidence`

- The next step is to place into a new file called `sugar_web_evidence` the following data:

    - Which web log file contains Sugar's IP address

    - The number of Sugar IPs addresses found in this file
    
 - Access the `web_logs` directory by going back a directory (`cd ..`), then:

   - `cd web_logs`

- To find the log files that have the IP address of `13.16.23.234` and place them in a new file called `sugar_web_evidence`, run:

   - `grep -il 13.16.23.234 * > sugar_web_evidence`
 
- Next, to append to this file the number of records that contain the IP address, run:
   
  - `grep -i 13.16.23.234 * | wc -l >> sugar_web_evidence`
    
- Now we move both evidence files to the `Sugar_evidence` directory that we created:

   - `cd ../../`

   - `mv ./Gathering_Evidence/email/sugar_email_evidence ./Gathering_Evidence/Sugar_evidence/`

   - `mv ./Gathering_Evidence/web_logs/sugar_web_evidence ./Gathering_Evidence/Sugar_evidence/`  
         
- Next, navigate to the `Sugar_evidence` directory, and concatenate the files into a single file called `Sugar_evidence_for_authorities`:

  - `cd Gathering_Evidence/Sugar_evidence/` 

  - `cat sugar_email_evidence sugar_web_evidence > Sugar_evidence_for_authorities`
  
- The last step is to confirm the file has the correct data for the authorities. Run: 

  - `cat Sugar_evidence_for_authorities`

 - The results should be:

      ```
      email5 
      email7  
      email8  
      3
      0518weblog 
      22
      ```
     
     While this file contains all the data the authorities need, this is not obvious. In the next lesson, we'll learn how to edit the contents of a file to further describe the evidence. 
     
--- 
&copy; 2023 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
