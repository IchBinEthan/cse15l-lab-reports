# Lab Report 3

In this Lab Report assignment, I used the `find` command. 

## `less -N`;

The command `less -N` numbers out the lines of the file and then prints them out.

While may not be noteworthy, the indexing indeed starts from 1 (as opposed to, say, 0 -- like in array indexing). So the number 1 refers to the first line, 2 for the second, and so on.

**How is this command important?** It becomes easier to refereence pieces of code by their location in the file. For example, a programmer can realize where a mistake was made in the file and place an exact location on it based on which line it was.

Here are instances of the command `less -N` being used for two different files: `pmed.0020085.txt` and `Fire_Victims_Sue.txt` respectively.


``` $ less -N ./technical/plos/pmed.0020085.txt ```
```
      1 
      2   
      3     
      4       
      5         
      6         We appreciate the note from Drs. Koudinov and Berezov [1]. In our opinion, no model has
      7         yet been presented that plausibly accounts for all the data on statins, cholesterol,
      8         amyloid-<C3><9F> protein (A<C3><9F>), and Alzheimer disease. In our paper [2], we present evidence that
      9         the isoprenoid pathway contributes to statin-activated shedding of the APP ectodomain in
     10         cultured cells. We do not yet know which (if any) other <E2><80><9C>cholesterol-related<E2><80><9D> Alzheimer
     11         phenomena are also attributable to modulation of isoprenoids, Rho, or ROCK.
     12         Previously, conventional wisdom held that A<C3><9F> load and hypercholesterolemia were directly
     13         related, based on observations that high-fat diet aggravated amyloid pathology in
     14         plaque-forming mice [3,4,5]. More recently, however, the formulation that statins act
     15         simply via cholesterol-lowering fails to account for several observations that cannot
     16         immediately be reconciled, either with the original <E2><80><9C>dogma<E2><80><9D> or with each other.
     17         First, Fagan et al. [6] questioned the role of cholesterol as the final common pathway
     18         in A<C3><9F> load specification, since, in their experiments, low cholesterol per se apparently
     19         had no impact on brain A<C3><9F> load in plaque-forming transgenic mice. Then, equally puzzling
     20         pharmacological data emerged. Atorvastatin was shown to lower brain amyloid load and A<C3><9F>
     21         levels, but brain cholesterol levels were unaffected by the drug [7]. In an apparent
     22         complete contradiction with the original observations, now, some investigators have been
     23         able to devise circumstances under which there is an inverse relationship between
     24         cholesterol and A<C3><9F>, with low neuronal cholesterol increasing A<C3><9F> generation [8], and vice
     25         versa [9]. These newer observations are unexpected and extremely puzzling, and no
     26         comprehensive explanation has yet emerged.
     27         For those readers seeking an update on this challenging area, we would direct your
     28         attention to the Alzheimer Research Forum Web page
     29         (http://www.alzforum.org/new/detailprint.asp?id=1135), where you will find an excellent
     30         review of the literature as well as a series of evaluations of how our data fit into
     31         existing scenarios and models regarding cholesterol, statins, cerebral amyloidosis, and the
     32         cognitive failure of Alzheimer disease.
     33       
     34     
     35    
```


```$ less -N ./technical/government/Media/Fire_Victims_Sue.txt  ```

```
      1 
      2 
      3 
      4 
      5 Kalamazoo Gazette
      6 
      7 Alamo Fire Victims Sue Landlord
      8 By Craig McCool
      9 Thursday, August 8, 2002
     10 Nine families displaced by a fire at Alamo Hills Apartments in
     11 March filed lawsuits Wednesday against the apartment complex.
     12 They allege that the complex could have done more to protect
     13 belongings they were forced to abandon in the aftermath of the
     14 blaze.
     15 Bernard Dempsey Jr., an attorney with Western Michigan Legal
     16 Services, the group that represents the tenants, said Alamo Hills
     17 gave the displaced families very limited opportunity to remove
     18 belongings.
     19 "They were given three days to get their stuff out, and if they
     20 couldn't get moved out in three days, their stuff was discarded,"
     21 Dempsey said. "Alamo Hills just threw it out."
     22 Others, he said, lost possessions to looters after the March 23
     23 blaze, which left 78 people temporarily homeless.
     24 According to the lawsuit, the tenants were prohibited from
     25 entering their apartments to retrieve possessions and were promised
     26 that the complex would provide security.
     27 A spokesperson for PM One, the company that manages Alamo Hills,
     28 could not be reached for comment.
     29 Nine separate suits were filed in 8th District Court, which
     30 handles civil claims of less than $25,000.
     31 "We're asking for the reimbursement of the value of their
     32 property and a small amount for stress -- $3,000 on top of their
     33 out-of-pocket expenses for their lost stuff," Dempsey said.
     34 "They're not looking to get rich off this. A lot of this is
     35 simply because they were treated so badly."
     36 Dempsey said most of the tenants who filed suits still live at
     37 the apartment complex, although many are trying to find homes
     38 elsewhere.
     39 "The new apartments (they were provided) were not in very good
     40 shape. That's actually one of the claims," he said.
     41 
     42 
     43 
     44 
  ```
  
## `less +`;
  
The command `less +` returns the contents of files by its lines, but view from a different position than the start. Unlke `less -N`, it does not number them. The command is used with a reference to the line that the programmer wants to start viewing from.

For example, say I wish to view lines `20` and beyond of some file `fileName.txt`. The correct way to implement the command is to append `20` to `less +`: 

`$ less +20 ./fileName.txt`

**How is this command important?** This is used to make viewing files more efficiently. If, for example, I have a Java file that has a particular method whose code started at line `37`, viewing the contents starting from line 37 from the top would allow me to see the method I want to edit.  

Here are instances of the command `less +` being used for the same two files `pmed.0020085.txt` and `Fire_Victims_Sue.txt` respectively.

```less +6 ./technical/plos/pmed.0020085.txt ```

```
        We appreciate the note from Drs. Koudinov and Berezov [1]. In our opinion, no model has
        yet been presented that plausibly accounts for all the data on statins, cholesterol,
        amyloid-<C3><9F> protein (A<C3><9F>), and Alzheimer disease. In our paper [2], we present evidence that
        the isoprenoid pathway contributes to statin-activated shedding of the APP ectodomain in
        cultured cells. We do not yet know which (if any) other <E2><80><9C>cholesterol-related<E2><80><9D> Alzheimer
        phenomena are also attributable to modulation of isoprenoids, Rho, or ROCK.
        Previously, conventional wisdom held that A<C3><9F> load and hypercholesterolemia were directly
        related, based on observations that high-fat diet aggravated amyloid pathology in
        plaque-forming mice [3,4,5]. More recently, however, the formulation that statins act
        simply via cholesterol-lowering fails to account for several observations that cannot
        immediately be reconciled, either with the original <E2><80><9C>dogma<E2><80><9D> or with each other.
        First, Fagan et al. [6] questioned the role of cholesterol as the final common pathway
        in A<C3><9F> load specification, since, in their experiments, low cholesterol per se apparently
        had no impact on brain A<C3><9F> load in plaque-forming transgenic mice. Then, equally puzzling
        pharmacological data emerged. Atorvastatin was shown to lower brain amyloid load and A<C3><9F>
        levels, but brain cholesterol levels were unaffected by the drug [7]. In an apparent
        complete contradiction with the original observations, now, some investigators have been
        able to devise circumstances under which there is an inverse relationship between
        cholesterol and A<C3><9F>, with low neuronal cholesterol increasing A<C3><9F> generation [8], and vice
        versa [9]. These newer observations are unexpected and extremely puzzling, and no
        comprehensive explanation has yet emerged.
        For those readers seeking an update on this challenging area, we would direct your
        attention to the Alzheimer Research Forum Web page
        (http://www.alzforum.org/new/detailprint.asp?id=1135), where you will find an excellent
        review of the literature as well as a series of evaluations of how our data fit into
        existing scenarios and models regarding cholesterol, statins, cerebral amyloidosis, and the
        cognitive failure of Alzheimer disease.
      
    
  ```
In the file `/pmed.0020085.txt`, we noticed originally that the file's first line of content started at line 6 through using `less -N`. Therefore, if I wanted to view the line of the file from the first line of content, I could call `less +6` into the command line with this file to get rid of unnecessary empty lines at the top while viewing.





``` $ less +5 ./technical/government/Media/Fire_Victims_Sue.txt  ```

```
Kalamazoo Gazette

Alamo Fire Victims Sue Landlord
By Craig McCool
Thursday, August 8, 2002
Nine families displaced by a fire at Alamo Hills Apartments in
March filed lawsuits Wednesday against the apartment complex.
They allege that the complex could have done more to protect
belongings they were forced to abandon in the aftermath of the
blaze.
Bernard Dempsey Jr., an attorney with Western Michigan Legal
Services, the group that represents the tenants, said Alamo Hills
gave the displaced families very limited opportunity to remove
belongings.
"They were given three days to get their stuff out, and if they
couldn't get moved out in three days, their stuff was discarded,"
Dempsey said. "Alamo Hills just threw it out."
Others, he said, lost possessions to looters after the March 23
blaze, which left 78 people temporarily homeless.
According to the lawsuit, the tenants were prohibited from
entering their apartments to retrieve possessions and were promised
that the complex would provide security.
A spokesperson for PM One, the company that manages Alamo Hills,
could not be reached for comment.
Nine separate suits were filed in 8th District Court, which
handles civil claims of less than $25,000.
"We're asking for the reimbursement of the value of their
property and a small amount for stress -- $3,000 on top of their
out-of-pocket expenses for their lost stuff," Dempsey said.
"They're not looking to get rich off this. A lot of this is
simply because they were treated so badly."
Dempsey said most of the tenants who filed suits still live at
the apartment complex, although many are trying to find homes
elsewhere.
"The new apartments (they were provided) were not in very good
shape. That's actually one of the claims," he said.




```

Similarly for this example, `Fire_Victims_Sue.txt` originally has the first four lines empty. I can also shift my view to ignore those lines and view the beginning of the content at the top of my page by using the command to start viewing from line 5.

  
