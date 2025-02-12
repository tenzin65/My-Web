<h1>How to Analyze Malicious Microsoft Office Files</h1><br>
<h3>Handling Malicious Microsoft Office Files During Incident Response</h3>
Incident response team will collect suspicious files and evidence from the compromised endpoint in order to investigate the incident.<br>
The main challenges IR team face is finding the malicious files which are used to attack and classifing them in gropu or same family.<br>
Binary files(0/1) The main suspect files are binary file as the malicious code are executed within the normal code or  attached to an email .<br>
<h3>Types of Microsoft Office File Formats</h3>
xml- It is based on a tree structure and each ooxml file contain a .xml file.<br>
OOXML(ofice open xml)- It is zipped xml based format develop by MS and used for all MS office file.<br>
Rich Text File(RTF)- is a another document formate which has a text and graphic combine together which make it easy to share the file between application.<br> 
<h3>Why Document Files Can be Dangerous and How to Analyze Them</h3>
Office Macros<br>
It save user time by allowing them to automate a series of command which are triggered by different actions.It is written in Visual Basic for application, it is a language which is support by all the MS office product.We can also create it by recording it within the MS application.
<h3>Abusing Windows Dynamic Data Exchange (DDE)</h3>
It is a protocol that is used to share data between MS tools or application.object linking and embedding is able to share data using this protocol.