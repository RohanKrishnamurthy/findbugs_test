# findbugs_test

FindBugs + security plugin Docker container

Run process:
```
docker pull rohank14/findbugs_test
```

Assuming the code to be analyzed is placed in 'src' directory or change the last parameter from src to the folder name to be analyzed.


Run the container: 


1: With error in CLI:
```
docker run --rm  -v `pwd`:/workdir/src rohank14/findbugs-sec src
```

2. With error reported in HTML format:
```
docker run --rm -v `pwd`:/workdir/src lokori/findbugs-sec -html -output /workdir/src/findsec-report.html src
```
3. With error reported in HTML format - a bit fancy user interface
```
docker run --rm -v `pwd`:/workdir/src lokori/findbugs-sec -html:fancy-hist.xsl -effort:max -relaxed  -output /workdir/src/findsec-report.html src
```
