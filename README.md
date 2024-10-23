<h1>Comparing Files with Hash Values</h1>

<h2>Description</h2>
This project focuses on the creation and comparison of hash values to evaluate data integrity and security. I will explore the process of generating hash values for files, followed by utilizing the <code>cmp</code> command to analyze and compare these hash files. Through this investigation, I will uncover potential discrepancies between files that may initially appear identical, highlighting the importance of thorough data evaluation before making informed business decisions.

<h2>Languages and Utilities Used</h2>

- <b>Shell Commands</b>

<h2>Environments Used</h2>

- <b>Linux</b>

<h2>Program Walk-through:</h2>

<h3>1. Generate Hashes for Files</h3>
<p align="center">
<img src="https://i.imgur.com/2XCnqYJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
After displaying the files in the directory I want to look at this contents. The command <code>cat file1.txt</code> and <code>cat file2.txt</code> displays the same result. In order to be sure that they are the same file, I would like to look at thier hash values. SHA-256 (Secure Hash Algorithm 256-bit) is a cryptographic hash function that produces a fixed-size, 256-bit hash value from input data, regardless of its size. SHA-256 helps verify the integrity of files. By comparing the hash value of a file before and after transfer or storage, you can determine if the file has been altered or corrupted. 
<br/>
The commands used to generate the hash values are <code>sha256sum file1.txt</code> and <code>sha256sum file2.txt</code>
<br/>
<br/>

**Cybersecurity Application:** SHA-256 is critical in cybersecurity for maintaining data integrity, securing communications, and verifying the authenticity of digital assets.
 
<h3>2. Comparing Hash Values</h3>
<p align="center">
<img src="https://i.imgur.com/oFBeorY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
I want to append the output of the hash creation command of both files into files named file1hash and file2hash respectively. If they do not exist, they will be created. If they do exist, the new hash value will be added to the end of their respective file without overwriting the existing content. I have displayed both files and their hashes for clarity.
<br/>
<br/>
<p align="center">
<img src="https://i.imgur.com/YtshWYm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<code>cmp file1hash file2hash</code>: The <code>cmp</code> command is used to highlight the differences in the file1hash and file2hash files. The output indicates that the hashes differ in the first character in the first line. 
<br/>
<br/>

**Cybersecurity Application:** It is crucial to know if files have been altered. I can verify whether two sets of data (or files) have the same hash value. If the hashes match, it indicates that the files are identical, confirming that data integrity has been maintained.


<h2>Conclusion</h2>
Creating hash values and utilizing the <code>cmp</code> command to compare hash files is an effective method for enhancing data integrity and security across various applications. This process is essential for ensuring the reliability and protection of data within an organization. In this project, while two files initially appeared to have identical contents, a more thorough inspection revealed differences between them. Consequently, further evaluation is warranted before proceeding with any business plans involving these files.
