#### Huffman-Text-Compression-and-Decompression

<p>Text files can be compressed to make them smaller and faster to send, and unzipping files on devices has a low overhead. The process of    encoding involves changing the representation of a file so that the (binary) compressed output takes less space to store and takes less time to transmit while retaining the ability to reconstruct the original file exactly from its compressed representation. Text files can be of various #file types, such as HTML, JavaScript, CSS, .txt, and so on. Text compression is required because uncompressed data can take up a lot of space, #which is inconvenient for device storage and file sharing.</p>
<h3>Text Compression :</h3>
The size of the text file can be reduced by compressing it, which converts the text to a smaller format that takes up less space. It typically
works by locating similar strings/characters within a text file and replacing them with a temporary binary representation to reduce the overall file size.
<p>Lossless compression can restore all elements of a file during decompression without sacrificing data and quality.</p>
<p>The two methods differ in the length of the codes. Analysis shows that variable-length encoding is much better than fixed-length encoding. Characters in variable-length encoding are assigned a variable number of bits based on their frequency in the given text. As a result, some characters may require a single bit, while others may require two bits, while still others may require three bits, and so on.</p>
<p>Huffman coding compresses text using following steps :</p>
<p>The algorithm works by first determining all of the file's unique characters and their frequencies.</p> 
<p>The characters and frequencies are then added to a Min-heap.</p> 
<p>It then extracts two minimum frequency characters and adds them as nodes to a dummy root.</p>
<p>The value of this dummy root is the combined frequency of its nodes and this root node is added back to the Min-heap.</p>
<p>The procedure is then repeated until there is only one element left in the Min-heap.</p>
<h3>Decompressing the Compressed Text :<h3>
<p>The compressed file is opened, and the number of unique characters and the total number of characters in the file are retrieved.</p>
<p>The characters and their binary codes are then read from the file. We can recreate the Huffman tree using this.</p>
<p>For each binary code:</p> 
<p>1.A left edge is created for 0, and a right edge is created for 1.</p> 
<p>2.Finally, a leaf node is formed and the character is stored within it.</p>
<p>3.This is repeated for all characters and binary codes. The Huffman tree is thus recreated in this manner.</p>
<p>4.The remaining file is now read bit by bit, and the corresponding 0/1 bit in the tree is traversed. The corresponding character is written into the decompressed file as soon as a leaf node is encountered in the tree.</p>
<p>5.Step 4 is repeated until the compressed file has been read completely.</p> 
