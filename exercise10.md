# Exercise 10 - Understanding Commits

1. Look at your commit log

        git log --oneline

2. Choose a commit hash

3. See what type of object that hash names

        git cat-file -t <hash>

        commit

4. Examine the contents of that commit closely

        git cat-file -p <hash>

C:\Users\Alex\CISW24\my_repository>git cat-file -p f424eb3
tree e3329e3fe34bd16d3cea33d57f484a41aa30536b
parent b2d15c25fe57c938b81e25f8e3c71710b4f99eef
author vit4l1ze <vit41lze@gmail.com> 1665298711 -0700
committer vit4l1ze <vit41lze@gmail.com> 1665298711 -0700

Adding new files
5. Find the parent's hash in the commit log

parent b2d15c25fe57c938b81e25f8e3c71710b4f99eef

6. Look at the contents of the tree

        git cat-file -p <hash>

C:\Users\Alex\CISW24\my_repository>git cat-file -p e3329e3fe34bd16d3cea33d57f484a41aa30536b
100644 blob d7ab22325fa2ab2e590e52d0586a34122b4a7d28    appliances.txt
100644 blob e69de29bb2d1d6434b8b29ae775ad8c2e48c5391    equipment.txt
100644 blob 5c76334361927824661bf002c9363a6548f63173    fruits.txt
100644 blob 84fa0b7fd736e95b8957bcde44d113202842861a    vegetables.txt        

7. Examine the contents of one of the blobs

100644 blob 5c76334361927824661bf002c9363a6548f63173    fruits.txt

8. What type of object does the parent hash represent?

        git cat-file -t <hash>

        commit

9. Examine the contents of the parent and its tree

10. Do the trees you looked at have any matching hashes listed?
        No they do not