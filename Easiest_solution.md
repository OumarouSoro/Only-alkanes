1. On your github account, create a github repo named "Only alkanes"
   After connecting to my github account, I went to repository then clicked on new repository, entered the name Only_alkakanes then I clicked on create new repository

2. Clone the newly created repo to your local machine
on my machine terminal, I entered this code ``git clone` <repository link>` the copied the link of my new repository from the github account and then pasted it before pressing on enter key.
3. Copy the contents of alkanes folder from shell-lesson-data/exercise-data/, used in previous classes, into your "Only alkanes" repo
   For this I used the following command `cp -r alkanes/* ../../Only-alkanes`

4. Run the following command while inside the repo `for j in `ls *.pdb`; do for k in {1..100}; do cp $j $(basename -s .pdb $j)$k.pdb; done; done
`
5. Find the easiest way to push only the .pdb files whose number suffix is divisible by 10

6. Document your answer/work-around for the task number 5 in a markdown file named "Easiest solution.md"

This is the easiest way to do it, run a script

#!/bin/bash

for file in $(ls *0.pdb); do
  git add "$file"
done

git commit -m "Add .pdb files divisible by 10"
git push
