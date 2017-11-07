# FirstMondays-runbwa
git repo from the November 6, 2017 "First Mondays" presentation: ""A workflow for implementing HTCondor Pipelines" 

Problem: Building binaries for CHTC can be problematic.

Workflow:  Two ideas to alleviate the pain:

	   1. Build on a CentOS 7 platform that's more friendly to users.
	   2. Use Git to manage the environment.


High-level view:

Step 1:  Get the binary running on pink.botany.wisc.edu.  Capture the environment in a (local) git repository.
     
Step 2:  Propogate the git repository to a "remote" server.

Step 3:  Fire up an interactive HTCondor job, as usual.

Step 4:  Clone the repo on the execute node and test.  Push changes to the remote repo.

Step 5:  Deploy as a noninteractive job, as usual.
