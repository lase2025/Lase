# Lase

###### Experimental results

**exp1_result**

- The coverage result is in result1.tar.gz. Our experiment involves 6 modes, including DFS, BFS, GSDSE, NS, GS_DFS, GS_BFS and each mode was run in 3 times. So you can see DFS0, DFS1, DFS2 ... in result1.tar.gz. 
- Under the file path of each mode, you can see 4-5 subfolders, such as Coverage (coverage results) , inputStr (inputs generated in experiment), nohup (running output）, TokenSeq(token sequence corresponding to  and token summaries) and results (grammars).  
- The coverage results of parsers is in cov.txt, collected from benchname_0.csv in Coverage folders.
- The coverage results of functional code is in cov1.txt, collected from benchname_Janino.csv,  benchname_Cloli.csv,  benchname_Simplecsharp.csv,  benchname_Jphp.csv and benchname_Jscript.csv in Coverage folders.

**exp2_result**

- Results related to grammar synthesis are in result2.tar.gz, including lark-results, arvada-results and treevada-results.
- For each benchmark in lark-results, there are 4 modes (i.e., Lase, Glade-t, Glade, Lase-c) and you can find out the synthesized grammar, precision, recall and synthesis time in the folders.
- For arvada and treevada, you can see the synthesis time in GADSE_benchname_round.log ,and grammar, precision and recall in  GADSE_benchname_round.log.eval.
- Note that for "selfdef7", we evaluate recall in parallel for acceleration.



###### Reproduce the results

We provide a docker image for you to reproduce the results. 

- docker pull lase2025/lase_oopsla25:latest	       *#pull the docker images*
- docker images            *#check the docker*
- docker run -it lase2025/lase_oopsla25:latest /bin/bash
- cd /home/Lase && ./run_all.sh               *#run all experiments*
- cd /home/Lase/DSE/gencov  && python3 computeAver.py               *#get cov.txt and cov1.txt*

