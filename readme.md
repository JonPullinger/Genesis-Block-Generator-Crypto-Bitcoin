This is the readme.md file for GenBlock0.c a genesis block creator for a new blockchain.

Firstly, I am using a Mac and assume you have installed Home Brew (now includes OpenSSL) and xcode.  
Ensure you get the full version of home brew and the shallow version.  I know Mac user and shallow - who would have guessed it. ;)
This is how I built the genesis block creator - it's not the only one and it's not the only way/. I'm comfortable in C and therefore 
used C.  Ok now for the important parts.

<b>Step One</b>

1.  Open a terminal on your Mac
2.  Type the following; <b>nano genblock0.c</b>
3.  Copy and paste the genblock0.c file from this Github repo into the terminal
4.  Press ctrl and x
5.  Press Y


<b>Step Two</b>

Now you have successfully created the c file we shall be using shortly.  Next step is to compile it. For this we do the following;

Type the following command into the terminal; <b>gcc genblock0.c -o genblock0 -lcrypto</b>

This will complie the file and reference the correct libraries for you automatically.  Now for the fun part, creating your very own 
genesis block.

<b> Step Three </b>

A genesis block is created using a Public Key, a TimeStamp and nBITS (see: https://bitcoin.org/en/developer-reference#target-nbits) for
a detailed explaination.  This is is presented to the program in the following format.

<b>./genblock0 04678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5f "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks" 486604799</b>

The above command is very long so please ensure you copy it correctly for testing purposes.

If you have followed this correctly you will recieve the following output;

Coinbase: 04ffff001d0104455468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73

PubkeyScript: 4104678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5fac

Merkle Hash: 3ba3edfd7a7b12b27ac72c3e67768f617fc81bc3888a51323a9fb8aa4b1e5e4a
Byteswapped: 4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b
<br>Generating block...
