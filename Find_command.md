## Find command

find y backup --> find . -maxdepth 3 -name '*.xml' -exec tar -rvf out.tar {} \;

find and count occurences in files --> grep -rI 'CSCFC002' . | cut -d : -f 1 | uniq -c

Output:

    412 ./SGA1_OBS_OAS__VAL_STK________G20200901141540Z.ssf
    824 ./SGA1_101_GMV__VAL_STK________G20200901141440Z.ssf
    824 ./SGA1_OBS_OAS__VAL_STK________G20200901141440Z.ssf
    412 ./SGA1_OBS_OAS__VAL_STK________G20200901141510Z.ssf
    412 ./SGA1_102_GMV__VAL_STK________G20200901141510Z.ssf
    412 ./SGA1_103_GMV__VAL_STK________G20200901141540Z.ssf

find without following mount devices --> find / -mount -name .vimrc

find links to file --> find / -lname /path/to/original/dir

find . -type f | xargs command --> apply a command to all files recursive

find . -type l -l                               --> list symbolic links

find . -mmin 5                               --> list files modified in the last 5 minutes

find dirs with name and print contents -->
find . -name resources -print -exec ls {} \;



https://superuser.com/questions/229410/find-grep-command-without-searching-mounted-shares
https://askubuntu.com/questions/429247/how-to-find-and-list-all-the-symbolic-links-created-for-a-particular-file