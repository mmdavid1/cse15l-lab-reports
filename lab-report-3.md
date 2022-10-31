<h1>Lab Report  3</h1>

<p>I have chosen to use the command <b>find</b>, and the first option for find that I am using is <b>-size</b>, which returns files based on a size parameter that you give it </P>

<h2>-size</h2>
1. Input: (size parameter is 200 Kilobytes, so it returns files that are larger than +200 KB)

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical -size +200k

Output:

        ./technical/government/About_LSC/commission_report.txt
        ./technical/government/Env_Prot_Agen/bill.txt
        ./technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
        ./technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
        ./technical/government/Gen_Account_Office/d01591sp.txt
        ./technical/911report/chapter-13.4.txt
        ./technical/911report/chapter-13.5.txt
        ./technical/911report/chapter-3.txt

<p>Explanation: The command -size returns the files that match your given size parameter, it can be either + or - and it can be G (Gigabyte), k (Kilobyte), M (Megabyte), etc. This is useful if for example you are trying to see what files are taking up a lot of space in your computer</p>

<p>2. Input: size +1M, will return files larger than 1 MB</P>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/biomed -size +1M 

<p>output:</p>
        
        [Empty]
<p>This output means that there are no files that are larger than 1MB in the biomed folder, so if for some reason you wanted to limit your file size this is one way to sort through file sizes</p>

<p>3. <b>Input:</b> </P>
            
             matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -2k

<p><b>Output: </b></P>

        ./technical/plos/pmed.0020048.txt
        ./technical/plos/pmed.0020028.txt
        ./technical/plos/pmed.0020191.txt
        ./technical/plos/pmed.0020226.txt
        ./technical/plos/pmed.0020192.txt
        ./technical/plos/pmed.0020157.txt
        ./technical/plos/pmed.0020082.txt
        ./technical/plos/pmed.0020120.txt

<p>This output means that there are the files that are under 2 KB in size within the plos folder, showing the smaller files in the folder, which can be helpful if you are trying to determine which file sizes are the smallest</P>

<br>
<br>
<p>The next command line option I am going to be using is -ls</P>

<h2>-ls</h2>

<p><b>Input:</b> </p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -2k -ls

<p>The input here is using both -size -2k and -ls, the size (described above) is simply put in to minimize the amount of files in the output (limits the files to those under 2KB). What -ls does is that it list the file along with useful information about the file, </p>

<p><b>Output:</b> </p>

        20290347        8 -rwxr-xr-x    1 matthewdavid     staff                1342 Oct 26 12:01 ./technical/plos/pmed.0020048.txt
        20290338        8 -rwxr-xr-x    1 matthewdavid     staff                2016 Oct 26 12:01 ./technical/plos/pmed.0020028.txt
        20290399        8 -rwxr-xr-x    1 matthewdavid     staff                 876 Oct 26 12:01 ./technical/plos/pmed.0020191.txt
        20290415        8 -rwxr-xr-x    1 matthewdavid     staff                 920 Oct 26 12:01 ./technical/plos/pmed.0020226.txt
        20290400        8 -rwxr-xr-x    1 matthewdavid     staff                1042 Oct 26 12:01 ./technical/plos/pmed.0020192.txt
        20290389        8 -rwxr-xr-x    1 matthewdavid     staff                1408 Oct 26 12:01 ./technical/plos/pmed.0020157.txt
        20290361        8 -rwxr-xr-x    1 matthewdavid     staff                1538 Oct 26 12:01 ./technical/plos/pmed.0020082.txt
        20290379        8 -rwxr-xr-x    1 matthewdavid     staff                1444 Oct 26 12:01 ./technical/plos/pmed.0020120.txt

<p>The output above shows the files in the directory plos under 2kb in size but also relevant info about hte file. It shows the permissions on the file (-rwxr) means readable, writable, executable by the user, while the date at the end is the last modification to the file, while the name Matthewdavid is the file owner and staff is the group, and the number after staff is the file size in bytes. This is useful in case you want to see who owns the file, and the permissions that people have on the file</P>

<br>
<p><b>Input: </b></p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/biomed -size -10k -ls


<p><b>Output: </b></p>

        20289519       24 -rwxr-xr-x    1 matthewdavid     staff                9952 Oct 26 12:01 ./technical/biomed/1472-6769-1-4.txt
        20289499       16 -rwxr-xr-x    1 matthewdavid     staff                6804 Oct 26 12:01 ./technical/biomed/1471-2490-3-2.txt
        20289411       16 -rwxr-xr-x    1 matthewdavid     staff                6297 Oct 26 12:01 ./technical/biomed/1471-2334-3-13.txt

<p>The output above shoows the list of files in technical/biomed that are under 10k and additional information (I use size -10k to limit the output in order to show the relevancy of the -ls command). We again get the permissions, (-rwxr), the owner of the file and group that it belongs to as well as the last time the file was modified. This again is useful in case you need to know who the file owner is to make edits on the file.</p>

<br>

<p><b>Input: </b></p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/ -size -2k  -ls

<p><b>Output: </b></p>

        20289034        0 drwxr-xr-x    6 matthewdavid     staff                 192 Oct 26 12:01 ./technical/
        20289891        0 drwxr-xr-x    8 matthewdavid     staff                 256 Oct 26 12:01 ./technical//government
        20289892        0 drwxr-xr-x   19 matthewdavid     staff                 608 Oct 26 12:01 ./technical//government/About_LSC
        20289915        0 drwxr-xr-x   16 matthewdavid     staff                 512 Oct 26 12:01 ./technical//government/Env_Prot_Agen
        20289910        0 drwxr-xr-x    6 matthewdavid     staff                 192 Oct 26 12:01 ./technical//government/Alcohol_Problems
        20290168        0 drwxr-xr-x   16 matthewdavid     staff                 512 Oct 26 12:01 ./technical//government/Post_Rate_Comm
        20290079        8 -rwxr-xr-x    1 matthewdavid     staff                2009 Oct 26 12:01 ./technical//government/Media/Helping_Hands.txt
        20290047        8 -rwxr-xr-x    1 matthewdavid     staff                1708 Oct 26 12:01 ./technical//government/Media/Campaign_Pays.txt
        20290066        8 -rwxr-xr-x    1 matthewdavid     staff                1757 Oct 26 12:01 ./technical//government/Media/Fire_Victims_Sue.txt
        20290053        8 -rwxr-xr-x    1 matthewdavid     staff                1941 Oct 26 12:01 ./technical//government/Media/Court_Keeps_Judge_From.txt
        20290084        8 -rwxr-xr-x    1 matthewdavid     staff                1999 Oct 26 12:01 ./technical//government/Media/It_Pays_to_Know.txt
        20290129        8 -rwxr-xr-x    1 matthewdavid     staff                1742 Oct 26 12:01 ./technical//government/Media/Self-Help_Website.txt
        20290086        8 -rwxr-xr-x    1 matthewdavid     staff                1741 Oct 26 12:01 ./technical//government/Media/Justice_requests.txt
        20290149        8 -rwxr-xr-x    1 matthewdavid     staff                2042 Oct 26 12:01 ./technical//government/Media/Wilmington_lawyer.txt
        20290091        8 -rwxr-xr-x    1 matthewdavid     staff                1992 Oct 26 12:01 ./technical//government/Media/Lawyer_Web_Survey.txt
        20290347        8 -rwxr-xr-x    1 matthewdavid     staff                1342 Oct 26 12:01 ./technical//plos/pmed.0020048.txt
        20290338        8 -rwxr-xr-x    1 matthewdavid     staff                2016 Oct 26 12:01 ./technical//plos/pmed.0020028.txt
        20290399        8 -rwxr-xr-x    1 matthewdavid     staff                 876 Oct 26 12:01 ./technical//plos/pmed.0020191.txt
        20290415        8 -rwxr-xr-x    1 matthewdavid     staff                 920 Oct 26 12:01 ./technical//plos/pmed.0020226.txt
        20290400        8 -rwxr-xr-x    1 matthewdavid     staff                1042 Oct 26 12:01 ./technical//plos/pmed.0020192.txt
        20290389        8 -rwxr-xr-x    1 matthewdavid     staff                1408 Oct 26 12:01 ./technical//plos/pmed.0020157.txt
        20290361        8 -rwxr-xr-x    1 matthewdavid     staff                1538 Oct 26 12:01 ./technical//plos/pmed.0020082.txt
        20290379        8 -rwxr-xr-x    1 matthewdavid     staff                1444 Oct 26 12:01 ./technical//plos/pmed.0020120.txt
        20289035        0 drwxr-xr-x   19 matthewdavid     staff                 608 Oct 26 12:01 ./technical//911report

<p>The output above shows all the files in ./technical which have a size less than 2 KB, and it again shows the permissions and other relevant information for the file, such as the permissions, owners, date modified, etc.</p>

<h2>-Delete</h2>

<p>Previous display: </p>

            matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/biomed -size -10k                 
            ./technical/biomed/1472-6769-1-4.txt
            ./technical/biomed/1471-2490-3-2.txt
            ./technical/biomed/1471-2334-3-13.txt

<p>Here we see that this command returns 3 files, now we will use -delete</p>

<p>input: </p>


    matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/biomed -size -10k -delete

<p>Now, if we run the same command as before, the output will be nothing, becuase -delete has deleted all the files which match the previous conditions</p>

<p>Output: </p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/biomed -size -10k        
        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 %  


<p>The -delete option has deleted all the files which match the previous condition from the folder, which can be useful when trying to organize folders and getting rid of old files which you no longer use.</p>

<br>

<p>Previous display:</p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -1k 
        ./technical/plos/pmed.0020191.txt
        ./technical/plos/pmed.0020226.txt

<p>Input: </p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -1k -delete

<p>Output: </p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % 

<p>Once again it shows that the files that match those specific conditions are deleted, this being useful for file organization and getting rid of files you no longer use</p>

<br>

<p>Previous display:</p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -3k
        ./technical/plos/pmed.0020048.txt
        ./technical/plos/pmed.0020074.txt
        ./technical/plos/pmed.0010029.txt
        ./technical/plos/pmed.0010067.txt
        ./technical/plos/pmed.0020028.txt
        ./technical/plos/pmed.0020027.txt
        ./technical/plos/pmed.0020024.txt
        ./technical/plos/pmed.0020192.txt
        ./technical/plos/pmed.0020145.txt
        ./technical/plos/pmed.0020021.txt
        ./technical/plos/pmed.0010068.txt
        ./technical/plos/pmed.0020022.txt
        ./technical/plos/pmed.0020157.txt
        ./technical/plos/pmed.0010025.txt
        ./technical/plos/pmed.0020086.txt
        ./technical/plos/pmed.0020085.txt
        ./technical/plos/pmed.0020278.txt
        ./technical/plos/pmed.0020082.txt
        ./technical/plos/pmed.0020120.txt
        ./technical/plos/pmed.0020281.txt

<p>Input: </p>


        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % find ./technical/plos -size -3k -delete

<p>Output: </p>

        matthewdavid@Matthews-MacBook-Air-3 skill-demo1 % 

<p>Here we see all the files in plos under 3 KB in size have been deleted, once again showing the power of -delete and how it can remove files from folders which is useful for organizing files and getting rid of files you no longer need</p>