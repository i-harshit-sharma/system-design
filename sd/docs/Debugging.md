# Debugging tips and tricks

## Keep in mind:

- Computer is logical and deterministic. If something is not working as expected, there is a reason for it.
- Being stuck is temporary.
- Know your limits and seek help from more knowledgeable people when needed.
- Fix things based on priority and some things are not worth fixing.

## Debugging Steps

### **Step 1** - Get as much information as possible about the issue.

- Get a screen recording, screenshot, detailed reproduction steps, logs and error messages resulting the issue.

### **Step 2** - Isolate the Environment.

- Check if the issue can be reproduced on the staging server or dev team's device. If not then it is likely an environment specific issue.
- Check for differences in software versions, configurations, network settings etc between prod and staging.

### **Step 3** - Reproduce the Issue.
1. **First step** - Create a timeline using print statements or use a debugger if possible.
2. **Still not able to reproduce?** 
    - Understand the scenario - some bugs occur only under specific conditions like high load, specific context or environment on customer devices.
    - Comb through stack traces and logs tofind line where error occurs. Recreate the lifecycle of the request leading to that line.
3. **Still Stuck?**
    - Get a break.
    - Ask someone
    - Rubber duck

### **Step 4** - Identify the Root Cause.
- Add logging, solve the problem and ship!

Good Luck with debugging!