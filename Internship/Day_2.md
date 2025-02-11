<h1>How to Analyze Malicious PDF Files</h1><br>
Portable Document Format (PDF) files are a cross-platform file format that supports links, images, and fonts. <br>
A phishing email is a fake email that scammers use to steal your passwords, bank details, or personal information.<br>
<h1>What is the PDF File Format?</h1>
The PDF format was created by Adobe in 1993, as a text-based structure that gives users a reliable way to present documents regardless of the operating system and the software they are using.<br><br>

```

xref(cross-Reference)-  It is used in different fields to link information between documents, databases, or code.<br>
xref
0 14
0000000000 65535 f<br>
0000000015 00000 n<br>
0000000660 00000 n<br>
0000000803 00000 n<br>
0000001007 00000 n<br>
0000001322 00000 n<br>
0000001049 00000 n<br>
0000001410 00000 n<br>
0000001200 00000 n<br>
0000001461 00000 n<br>
0000001513 00000 n<br>
0000001573 00000 n<br>
0000001632 00000 n<br>
0000001737 00000 n<br>
trailer<br>
<</Size 14/Root 12 0 R/Info 13 0 R/ID [<019e8b45c3227a3f8f35b7a9a09c2f70><019e8b45c3227a3f8f35b7a9a09c2f70>]>><br>
%iText-5.5.10<br>
startxref<br>
1901<br>
%%EOF<br>
```

peepdf- it is frre python tool which allow you to access  the details data of the pdf file.<br>
pdf-parser- it wiil allow you to inspact and extract the string and object from pdf.Also read, modify or analyzethe structure and content of a PDF document.<br>
eg-pdf-parser.py -f -o 18 -d extract_js files/example1.pdf.<br>
-f: it is use to filter the object.<br>
-o: it refers to the object<br>
-d: It refers to dump or save the file<br>
```
remnux@6866a79d9f93:~$ pdf-parser.py -o 8 -f -d drop_file2 exmple2.pdf <br>
obj 8 0<br>
 Type: /EmbeddedFile<br>
 Referencing:<br>
 Contains stream<br>

  <<<br>
    /Length 2004304<br>
    /Filter /FlateDecode<br>
    /Type /EmbeddedFile<br>
  >><br>
```