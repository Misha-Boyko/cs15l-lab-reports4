# Lab 4

## The steps I took to edit the file:
The first step I took was to ssh into the lab computer: 
```
ssh cs15lsp23bx@ieng6-201.ucsd.edu
```
![Image](Login.png)

I didn't have to type in the password after ssh because I had saved my ssh key onto the machine earlier. Therefore, when I login in from my computer now, the machine recognizes the corresponding key from my laptop and let's me in. I then cloned my fork of the lab7 on github and copy pasted the ssh clone link: 
```
git clone git@github.com:Misha-Boyko/lab7.gitgit@github.com:Misha-Boyko/lab7.git
```
![Image](GitClone.png)
Next I cd into the file I cloned by typing cd l and <tab> to complete the line to cd lab7. The <tab> completes the cd l command to cd lab7.
```
cd l <tab> <enter>
```
I then run the tests to show that it currently fails before any editing of the file.
I type bash te <tab> which auto compeltes to bash test.sh
```
bash te <tab> <enter>
```
![Image](TestFail.png)
The output shows that the tests failed so we need to edit the ListExamples file.
We edit the file by typing vim ListExamples. <tab> which autocompletes to vim ListExamples.java
```
vim ListExamples. <tab> <enter>
```
The vim terminal opens to the top of the page so we write the following commands to fix the error:
```
42 <enter>
e <enter>
r 2 <enter>
```
The terminal opens on the first line so by typing 42 <enter> we are sent to the 43rd line which is the line with the error in it. Then I type e which brings me to the end of the current word which was index1. The r 2 command replaces the "1" in index1 with a 2. The r does the replace and the "2" is what we replace the current character highlighted with.  
 
![Image](VimText.png)
 
After correcting the error we type :wq <enter> to save our changes.
```
:wq <enter>
```
To show that these changes fixed the error we run the tests again:
```
bash te <tab> <enter>
```
The "te" autocompletes to test.sh. The bash test.sh runs all of the tests again to show that the tests pass. 
![Image](TestPass.png)
Finally now that the changes have been fixed, we add, commit, and push the changes back to our repository:
```
git add . <enter>
git commit -m "Fixed final while loop indexing" <enter>
git push <enter>
```
![Image](GitChanges.png)
