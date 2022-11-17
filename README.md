# EBI Genome Bioinformatics: Introduction to Github

This is the code repository used for the "Introduction to Github" section of the EBI course [Genome Bioinformatics](https://www.ebi.ac.uk/training/events/genome-bioinformatics-resequencing-and-variant-calling-2022), named in previous years as "NGS Bioinformatics".

This sections follows the previous 3 days of the course, where command line tools and basic bioinformatics commands to index files and align fastqs to a reference genome have been acquired.
Here we focus on reusing the commands learnt during previous days, to modify an existing script and diff then commit changes.

The following README is a copy of the 2021 Google Docs walkthrough of the interactive part of the session.


## Modifying a Github Codebase
### Part 1: Fixing a forgotten command

1. To clone the repository to your own space, press the green code button and copy the URL by pressing the clipboard button
1. Go to the terminal in your VM and write `git clone` then right-click paste the URL
1. If you run `ls` after this you should see a new folder called 'EBI-Introduction-to-Github'
1. Inside this folder you should see the contents that you see on the github page you just cloned
1. Edit the bash script in the cloned folder, and add the command to index the fasta file to the beginning of the script
1. Run `git status` in the terminal to make sure git sees that your file has changed
1. Run `git diff` in the terminal to show what lines changed
1. add the changed file command to the git repository
1. Run `git status` again to see that git has now added the file.
1. commit the changes: use the `-m` argument and write what you’re committing
1. Run `git log` to see your list of commits


### Part 2: Optimisng Space

Now fixed, the script runs but produces these terribly large bam files. 
We remember learning about cram files and their improved storage efficiency. 
Lets modify the script once more, and add a command to the pipeline that will take the produced bam file, and convert it to a cram file.
Once we have a more efficient script we should remember to commit this change so everyone on Github, can see how efficient we are in genomics.

### Part 3: Viewing prior versions
Now you have improved and committed your script, you may want to see what you had before. Use `git log` to get the identifier of the commit before yours. You can turn back time in the git repository by running `git checkout` then the commit identifier. 

Have a look at the script at this point. You can return to present-day by running `git checkout main`.
