#How to Analyze Malicious PDF Files<br>
Portable Document Format (PDF) files are a cross-platform file format that supports links, images, and fonts. <br>
A phishing email is a fake email that scammers use to steal your passwords, bank details, or personal information.<br>
#What is the PDF File Format?
The PDF format was created by Adobe in 1993, as a text-based structure that gives users a reliable way to present documents regardless of the operating system and the software they are using.
#The PDF structure is hierarchical and contains four main parts: 

1. Header – Specifies the version number of the PDF.

2. The body – The document’s part that holds all of the information including text and other elements such as images, links, etc.

The body of the PDF file contains different objects which can reference each other, the objects have different types:

Names – /name backslash followed by ASCII characters – setting a unique name.
Strings – (text) its full syntax is a bit complex but what’s important is to know that it is enclosed in parentheses. 
Arrays – enclosed with square brackets ([...]) can contain other objects.
Dictionaries – table of key and value pairs. The key is a name object and the value can be any other object. Enclosed within double angle brackets (<<...>>)
Streams – contains embedded data structures like images (or code) which can be compressed. Streams represented by a dictionary that set the stream’s length with the key /Length and encoding /Filters.
Indirect object – object that has a unique ID, the object starts with the keyboard obj and ends with endobj other objects can reference the object using its ID. For example a reference to object with ID 3 we would look like this: 3 0 R
3. Cross-reference table – Specifies the offset from the start of the file to each object in the file, so that the PDF reader will be able to locate them without loading the whole document (it can save time when opening big files).
4. Trailer – Specifies information about the cross-reference table so the PDF reader will be able to find the table and other objects. PDF readers start reading the file from the end, let’s look at the example below:
xref(cross-Reference)-  It is used in different fields to link information between documents, databases, or code.
xref
0 14
0000000000 65535 f
0000000015 00000 n
0000000660 00000 n
0000000803 00000 n
0000001007 00000 n
0000001322 00000 n
0000001049 00000 n
0000001410 00000 n
0000001200 00000 n
0000001461 00000 n
0000001513 00000 n
0000001573 00000 n
0000001632 00000 n
0000001737 00000 n
trailer
<</Size 14/Root 12 0 R/Info 13 0 R/ID [<019e8b45c3227a3f8f35b7a9a09c2f70><019e8b45c3227a3f8f35b7a9a09c2f70>]>>
%iText-5.5.10
startxref
1901
%%EOF


peepdf- it is frre python tool which allow you to access  the details data of the pdf file.<br>
Output 
remnux@6262b6426ce2:~$ peepdf files/2e26d1a3d6547e15658033c8936c93474cd7a1b0214c98d9a2e575fa4017d123.sample
Warning: PyV8 is not installed!

File: 2e26d1a3d65d7e15658033c8936c93d74cd7a1b0214c98d902e575f040174123.sample
MD5: 2852936a7e33787c0ab11f346631d89
SHA1: 884010343aff0c3c5b97ac3dae94d04e81e24b2c
SHA256: 2e26d1a3d6547e15658033c8936c93d74cd7a1b0214c98d9a2e575fa40174123
Size: 76918 bytes

Version: 1.7

Binary: True
Linearized: False
Encrypted: False
Updates: 1
Objects: 21
Streams: 7
URIs: 1
Comments: 0
Errors: 0

Version 0:
Catalog: 15
Info: 13
Objects (15): [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15]
Streams (5): [7, 8, 9, 12, 14]
Encoded (4): [7, 8, 9, 12]
Objects with URIs (1): [5]
Suspicious elements:
/OpenAction (1): [15]
/Names (1): [15]

Version 1:
Catalog: 15
Info: 13
Objects (6): [13, 14, 15, 16, 17, 18]
Streams (2): [14, 18]
Encoded (1): [18]
Objects with JS code (1): [18]
Suspicious elements:
/OpenAction (1): [15]
/Names (2): [15, 16]
/JavaScript (2): [15, 17]
/JS (1): [17]

pdf-parser- it wiil allow you to inspact and extract the string and object from pdf.Also read, modify or analyzethe structure and content of a PDF document.
eg-pdf-parser.py -f -o 18 -d extract_js files/example1.pdf.
-f: it is use to filter the object.<br>
-o: it refers to the object<br>
-d: It refers to dump or save the file
remnux@6866a79d9f93:~$ pdf-parser.py -o 8 -f -d drop_file2 exmple2.pdf 
obj 8 0
 Type: /EmbeddedFile
 Referencing:
 Contains stream

  <<
    /Length 2004304
    /Filter /FlateDecode
    /Type /EmbeddedFile
  >>