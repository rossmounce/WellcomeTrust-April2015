# Document normalisation

## PLoS resource

We have downloaded 100 random files from PLoSONE from the (Europe) PMC web site. This shows how they are transformed to `scholarly.html` for use by `ami-plugins`. 

## Raw files

The filenames are of the form: `e0119090.xml`, etc. The files are in the NLM XML format, which is a format used by some publishers to expose articles for data mining. However, the format is complex and not always standardised, so we simplify and convert it to Scholarly HTML.
 
### Converting a single file to Scholarly HTML

None of the files is in ContentMine (CM) directory format, so we have to create this. Taking a single file

```
e0115544.xml
```
in the directory
```
~/workshop/02_ami/plos_one_latest_10/
```

### Creating a single `scholarly.html`

We can use the same directory and create a `scholarly.html` from the `fulltext.xml`.

```
norma -q ~/workshop/02_ami/plos_one_latest_10/e0115544 --input fulltext.xml --output scholarly.html --xsl nlm2html
```

read this as:
 * run `norma` as a transformer
 * on the CM directory `~/workshop/02_ami/plos_one_latest_10/e0115544`
 * use the file `fulltext.xml` in it as input
 * use the (XSL) stylesheet `nlm2html` to transform it
 * into the output `scholarly.html`

We have specifically developed the stylesheet for XML (such as PLoSONE) which conforms to `JATS` `NLM` . Only a few journals (BMC, Elsevier) use a different DTD and we can create those variants fairly easily. The output is:

```
NormaArgProcessor  - Writing : ~/workshop/02_ami/plos_one_latest_10/e0115544/scholarly.html
```
and if we list the directory:
```
localhost:norma pm286$ ls -lt ~/workshop/02_ami/plos_one_latest_10/e0115544/
total 488
-rw-r--r--  1 pm286  staff  146522 12 Apr 15:42 scholarly.html
-rw-r--r--  1 pm286  staff   99166 11 Apr 11:37 fulltext.xml
```

### multiple files

If we have 10, or 100 (or even more) files we need to automate the conversion. `norma` has a command to process all the files *within a directory*. We have directories in `~/workshop/02_ami/plos_one_latest_10/` :
```
localhost:norma pm286$ ls ~/workshop/02_ami/plos_one_latest_10/*
e0115544  e0116215  e0116596  e0116903  e0117956  e0118659  e0118685 
e0118692  e0118757  e0118792  e0119090
```
we want to convert them to `scholarly.html` :

Then we convert them. The top directory is `~/workshop/02_ami/plos_one_latest_10/`. It's not a CM directory but it has many child CM directories and converts each:

```
norma -q ~/workshop/02_ami/plos_one_latest_10/ -i fulltext.xml -o scholarly.html --xsl nlm2html
```

This means 
 * take the `~/workshop/02_ami/plos_one_latest_10/` as the directory to work in (`-q ...`)
 * look for all `fullext.xml` files (`-i fulltext.xml`)
 * convert them to scholarly HTML (`-o scholarly.html`)
 * using the NLM to HTML converter (`--xsl nlm2html`)

This command will create:

```
workshop@crunchbang:~/workshop/02_ami$ tree plos_one_latest_10
plos_one_latest_10
├── e0115544
│   ├── fulltext.xml
│   └── scholarly.html
├── e0116215
│   ├── fulltext.xml
│   └── scholarly.html
├── e0116596
│   ├── fulltext.xml
│   └── scholarly.html
├── e0116903
│   ├── fulltext.xml
│   └── scholarly.html
├── e0117956
│   ├── fulltext.xml
│   └── scholarly.html
├── e0118659
│   ├── fulltext.xml
│   └── scholarly.html
├── e0118685
│   ├── fulltext.xml
│   └── scholarly.html
├── e0118692
│   ├── fulltext.xml
│   └── scholarly.html
├── e0118757
│   ├── fulltext.xml
│   └── scholarly.html
├── e0118792
│   ├── fulltext.xml
│   └── scholarly.html
└── e0119090
    ├── fulltext.xml
    └── scholarly.html
```


 
