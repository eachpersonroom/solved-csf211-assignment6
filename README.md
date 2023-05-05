Download Link: https://assignmentchef.com/product/solved-csf211-assignment6
<br>
<strong>A: Disposition</strong>

Bob likes to watch the weather change so he wants to know today’s forecast. He has a list of <em>N </em>different numbers representing <em>a<sub>i</sub></em>, the air pressure at various times of the day. Bob can tell the weather using only these numbers, but to do so he first needs to sort them in non-decreasing order based on the value of <em>a<sub>i </sub></em>mod <em>k</em>, given <em>k</em>. For example, if <em>k </em>= 5 then the number 11 would come before 7 in the sorted array because 11 mod 5 is less than 7 mod 5. If the value of <em>a<sub>i </sub></em>mod <em>k </em>is equal to the value of <em>a<sub>j </sub></em>mod <em>k </em>for some <em>i </em>and <em>j</em>, then they must be sorted based on the values <em>a<sub>i </sub></em>and <em>a<sub>j </sub></em>(That is if <em>a<sub>i </sub>&lt; a<sub>j </sub></em>then <em>a<sub>i </sub></em>comes before <em>a<sub>j</sub></em>). Sort the array in this way for Bob.

<strong>Input</strong>

The first line contains two integers <em>N </em>and <em>k </em>as described above (1 ≤ <em>N </em>≤ 10<sup>5</sup>, 1 ≤ <em>k </em>≤ 10<sup>5</sup>). The second line of input contains <em>N </em>integers where the <em>i<sup>th </sup></em>number represents <em>a<sub>i </sub></em>(1 ≤ <em>a<sub>i </sub></em>≤ 10<sup>9</sup>).

<strong>Output</strong>

Print <em>N </em>integers in the sorted order as described in the question.

input

5 2

<ul>

 <li>2 3 4 5</li>

</ul>

output

<ul>

 <li>4 1 3 5</li>

</ul>

explanation

2 and 4 must come before the rest since they have a value 0 mod 2 and 1, 3, and 5 have a value 1 mod 2. Now 2 and 4 must be ordered based on their values and the same goes for 1<em>,</em>3<em>, </em>and 5.

<strong>B: Reflection</strong>

It soon becomes night and Bob likes to talk to the moon before going to sleep. The moon tells him that the light is not her own but that of a thousand reflections passing over her. Bob noticed a row of <em>N </em>pine trees that was illuminated by the light, the <em>i<sup>th </sup></em>pine tree having a height <em>h<sub>i</sub></em>. He decided that he wants them to be sorted in non-decreasing order. To do this, he can divide the entire array of trees into contiguous segments such that each tree belongs to exactly one segment. He can then sort all the elements within each segment in non-decreasing order independently from the other segments. He must now choose segments such that after performing this operation, the entire array of trees is sorted in non-decreasing order. Bob doesn’t want to waste energy on sorting so he wants to choose segments such that the number of segments chosen is as large as possible. Can you help Bob out?

<strong>Input</strong>

The first line contains an integer <em>N </em>representing the number of trees (1 ≤ <em>N </em>≤ 10<sup>5</sup>). The next line contains <em>N </em>numbers representing the height of the <em>i<sup>th </sup></em>tree <em>h<sub>i </sub></em>(1 ≤ <em>h<sub>i </sub></em>≤ 10<sup>9</sup>).

<strong>Output</strong>

Print a single integer, the largest possible number of segments you can choose satisfying the above conditions.

input 4

2 1 3 2

output 2

explanation

Here the optimal groups would be positions 1<em>,</em>2 in the first group and 3<em>,</em>4 in the second group. We can easily see that if we sort each segment individually the entire array will also be sorted.

<strong>C: Triad</strong>

Since this is the finale of Bob’s trilogy, he decides to keep quiet and let the work be done by a bunch of machines. Bob is actually a winemaker, but he’s a little weird and uses watermelons instead of grapes. He plans to use these machines to crush watermelons to use in his wine. There are <em>N </em>machines where the <em>i<sup>th </sup></em>machine takes time <em>t<sub>i </sub></em>to crush one watermelon. These machines can work simultaneously and independent of each other but one machine can only be crushing one watermelon at a time. You can assign a machine to begin crushing a watermelon at any time as long as the aforementioned rule is not violated. You can also use a machine more than once. Can you help Bob find the shortest amount of time needed to completely crush <em>k </em>watermelons?

<strong>Input</strong>

The first input line has two integers <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>5</sup>) and <em>k </em>(1 ≤ <em>k </em>≤ 10<sup>9</sup>): the number of machines and watermelons. The next line has <em>N </em>integers where <em>t<sub>i </sub></em>(1 ≤ <em>t<sub>i </sub></em>≤ 10<sup>9</sup>) represents the time needed for the <em>i<sup>th </sup></em>machine to crush one watermelon.

<strong>Output</strong>

Output a single integer representing the shortest time needed to completely crush <em>k </em>watermelons.

input

<h1>3 7</h1>

3 2 5

output 8

explanation

The optimal way in this case would be for machine 1 to crush two watermelons, machine 2 to crush 4 watermelons and machine 3 to crush 1 watermelon. This would take a total time of 8

<strong>D: ANC Orders</strong>

The ANC burger stall, which serves only one dish – Jalapen˜o Poppers, is open for <em>N </em>minutes every night. <strong>Each minute</strong>, <em>S<sub>i </sub></em>tired and hungry students return from the library and attempt to order a plate of Jalapen˜o Poppers. To order food, the ANC employee takes each student’s ID card and scans it with a barcode reader. The barcode scanner needs to be temporarily restarted in the  minute, and all students who arrive in these minutes will immediately leave (and will not come back) when they realise the barcode machine isn’t working. The owner has a backup barcode scanner that works perfectly for exactly <em>X </em>minutes, without requiring these maintenance cycles, and then shut down permanently. What would be the optimal time to activate this backup device, if the owner wants to serve as many students as possible?

<strong>Input</strong>

The first line contains two integers <em>N</em>, <em>k </em>and <em>X </em>(1 ≤ <em>k,X </em>≤ <em>N </em>≤ 5 × 10<sup>6</sup>), where <em>N </em>is the number of minutes the shop remains open and <em>k </em>is the number of minutes the barcode scanner doesn’t work. The next line contains <em>N </em>space separated integers <em>S</em><sub>0</sub><em>,S</em><sub>1</sub><em>,…S<sub>N</sub></em><sub>−1 </sub>denoting the number of students arriving in the zeroeth, first <em>… </em>(<em>N </em>− 1)<em><sup>th </sup></em>minute (1 ≤ <em>S<sub>i </sub></em>≤ 100). The third line of input contains <em>k </em>(sorted) space separated integers <em>r</em><sub>1</sub><em>,r</em><sub>2</sub><em>…r<sub>k </sub></em>meaning that the barcode scanner doesn’t work in these <em>k </em>minutes. Note that time here is 0-indexed.

<strong>Output</strong>

Print two space separated integers – (1) how many students the shop serves without the extra barcode machine and (2) the <em>maximal </em>number of students the shop could serve if it optimally uses the second barcode machine.

input

5 2 1

1 0 1 2 1

0 3

output

2 4

explanation

Since the backup barcode scanner can work for one minute exactly, we can choose to use it at time, <em>t </em>= 0 or <em>t </em>= 3. We choose <em>t </em>= 3 since more students are coming in then.

<strong>E: Anomaly Detection</strong>

Anomalies are points that don’t fit the “trend” of the rest of the data. Anomaly detection is the identification of rare items and points like these, representing that differ from the majority of the data by a lot. Rahul, a Data Scient PS2 intern at Macrobook, is attempting to implement a simple anomaly detection algorithm developed by research scientists at the company. Since Rahul has never written C code before, he approaches you for help. The algorithm is explained as follows:

You are given <em>N </em>data points each consisting of coordinates (<em>x<sub>i</sub>,y<sub>i</sub></em>), where both coordinates are not integers (guaranteed to be floats). It is guaranteed that all <em>N </em>points will lie inside the square formed by the points (0, 0), (C,0), (A,D), (0,D), where C and D are two positive integers. We divide the X-axis into C intervals (or buckets) – namely x=0 to x=1, x=1 to x=2 and so on till x = C-1 to x = C. Similarly, the Y-axis is divided into D equally spaced buckets of unit size. These intervals form a 2D grid in the plane, with each point being located inside one X bucket and one Y bucket each – let us call these <em>B</em>(<em>x<sub>i</sub></em>) and <em>B</em>(<em>y<sub>i</sub></em>) respectively. The algorithm then assigns a normality score to each point <em>N<sub>i </sub></em>= <em>count</em>(<em>B</em>(<em>x<sub>i</sub></em>)) ∗ <em>count</em>(<em>B</em>(<em>y<sub>i</sub></em>)), where <em>count</em>(<em>B</em>) represents the number of points in that specific bucket. The <em>k </em>points with the least normality scores are anomalies and should be outputted. If there is a tie in scores, resolve them by outputting the one with lesser index in the original array.

<strong>Input</strong>

<table>

 <tbody>

  <tr>

   <td width="122"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

The first line consists of four space separated integers N (1 ≤ <em>N </em>≤ 10<sup>7</sup>) , C, D (1 ≤ <em>C,D </em>≤ 10<sup>3</sup>), k (1 ≤ <em>k </em>≤ <em>N</em>). The next <em>N </em>lines contain two space separated floats each representing <em>x<sub>i </sub></em>and <em>y<sub>i </sub></em>(0 <em>&lt; x<sub>i </sub>&lt; C,</em>0 <em>&lt; y<sub>i </sub>&lt; D</em>) representing the <em>i<sup>th </sup></em>point, with <em>i </em>being zero-indexed.

<strong>Output</strong>

Print <em>k </em>space separated integers, representing the indices of the <em>k </em>anomalous points in non- order of normality scores.

input

4 10 10 2

3.1 3.2

3.3 7.7

9.1 3.2

0.1 2.9

output

<h1>3 1</h1>

explanation

The normality scores of the four points are 4, 2, 2, 1 respectively. The least score is of index 3’s so we output that. For the next highest we notice a tie between the

1st and 2nd index elements. We output the lesser of these indices, i.e. 1

<strong>F: Array Operations (Again)</strong>

You are initially given an array <em>A </em>and a set of <em>T </em>instructions that you must evaluate sequentially, in order. Each instruction <em>T </em>is a number <em>T<sub>i </sub></em>– which means that you should rotate the array left by <em>T<sub>i </sub></em>places. After executing each instruction, print the first and last element of the resulting array.

<strong>Input</strong>

The first line consists of two space separated integers, <em>N </em>and <em>T </em>(2 ≤ <em>T </em>≤ 10<sup>2</sup>), where <em>N </em>(0 <em>&lt; N &lt; </em>10<sup>4</sup>) is the size of the array <em>A </em>(0 ≤ <em>A<sub>i </sub></em>≤ 10<sup>9</sup>). The second line contains <em>N </em>space separated integers, the elements of <em>A</em>. The third line of input contains <em>T </em>space separated integers representing the instructions (0 ≤ <em>T<sub>i </sub></em>≤ <em>N</em>).

<strong>Output</strong>

Output <em>T </em>lines, each line containing two integers representing the first and last elements of the array after executing <em>i<sup>th </sup></em>query.

input

5 2

3 2 1 4 5

<ul>

 <li>2</li>

</ul>

output

<ul>

 <li>3</li>

</ul>

<h1>4 1</h1>

explanation after the first operation, the array becomes 2 1 4 5 3. After the second operation the array becomes 4 5 3 2 1.

<strong>G: Maximal Descendent Distance</strong>

You are given a binary tree, consisting of <strong>positive integer values </strong>only, and each node is guaranteed to have a <strong>unique </strong>value. The binary tree is represented as an array <em>A </em>of size <em>N</em>. <em>A</em>[0] is the root of the tree and for a given node <em>i</em>, (2<em>i</em>+1) and (21+2) represent the left and right child respectively. If <em>A</em>[<em>i</em>] = −1 for any <em>i</em>, that means that the node <em>i </em>does not exist. Given two numbers <em>a </em>and <em>b</em>:

<ul>

 <li>find the location of both of these in the binary tree. If any one or both of these keys don’t exist, print “-1”.</li>

 <li>Identify two nodes <em>a</em><sup>0 </sup>and <em>b</em><sup>0</sup>, which are <strong>leaf nodes </strong>and are descendants of <em>a </em>and <em>b </em>respectively, such that the <em>hamming distance between values stored in nodes a</em><sup>0 </sup><em>and b</em><sup>0 </sup><em>respectively is minimized</em>.</li>

 <li>Print one integer, representing this minimal hamming distance.</li>

</ul>

<em>Note: The hamming distance between two integers is defined as the number of bits that are different in the binary representations of the number. eg. Hamming distance between 3 (011) and 4 (100) is 3.</em>

<em>Note 2: Every node is considered to be a descendent of itself.</em>

<strong>Input</strong>

The first line consists of three space separated integer <em>N </em>(1 ≤ <em>N </em>≤ 10<sup>4</sup>), <em>a</em>, <em>b</em>. The next line consists of <em>N </em>space separated integers (<em>A<sub>i</sub></em>) representing the value of each node in the binary tree (1 ≤ <em>A<sub>i </sub></em>≤ 10<sup>5</sup>, or <em>A<sub>i </sub></em>= −1).

<strong>Output</strong>

Output one integer, the minimum hamming distance, as described in the problem.

input

7 2 3

1 2 3 -1 -1 4 5

output 2

explanation

The only possible leaf-descendent of 2 is 2. The possible leaf-descendants of 3 are 4 and 5. Hamming distance of (2, 4) = 2 and hamming distance of (2, 5) = 3. Minimal of these distances is the answer.

<strong>H: Special String Activities</strong>

You are given a string consisting of alphabets and brackets ”()[]”. It is guaranteed that the brackets are balanced. You need to process the string by:

<ul>

 <li>Reverse substrings that are located within “()”. For eg. (<em>aksj</em>) becomes <em>jska </em>after processing. (brackets removed).</li>

 <li>Increment all characters located within “[]”. For eg. [<em>abcd</em>] becomes <em>bcde </em>after processing (brackets removed). The character <em>z </em>would become <em>a </em>after incrementing.</li>

 <li>Process the brackets from innermost bracket to outermost bracket.</li>

</ul>

Print the processed string.

<strong>Input</strong>

The first line contains a string as described in the question above. It is guaranteed that the length of the string ≤ 10<sup>4</sup>.

<table>

 <tbody>

  <tr>

   <td width="122"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<strong>Output</strong>

Output one line, consisting of only lowercase English alphabets, denoting the processed string.

input abcdegfg output abcdegfg

input a(bc)deg[fg] output acbdeggh

input a(bc[de]gf)g output afgfecbg

input a[[[b]]]bujshs((dg)) output aebujshsdg

<strong>I: All Might vs The League of Villains</strong>

The league of villains was finally able to corner the great hero All Might. Underestimating his valor, they all decide to charge at him at once. As All Might’s sidekick, you (Dave) see the locations of all the villains and All Might as points (with X and Y coordinates) on your radar. You know that the bottom-most point (the minimum y-coordinate) on the radar corresponds to that of All Might. You recommend to fend off the villains in a in a single counter clockwise sweep (see sample case for clarity). Help All Might defend himself against the league of villains in a counter clockwise manner. If more than one villain has the same orientation with respect to All Might, you suggest All Might to first fend off the villain who is closer to him (in terms of manhattan distance). Assume that All Might does not move from his point.

<strong>Input</strong>

The first line of input contains a single integer N (2 ≤ N ≤ 10<sup>5</sup>) denoting the number of points on your radar. Each of the following N lines contain three space-separated integers P, <em>X<sub>P</sub></em>, <em>Y<sub>P </sub></em>(1 ≤ P ≤ N, −10<sup>9 </sup>≤ <em>X<sub>P </sub></em>, <em>Y<sub>P </sub></em>≤ 10<sup>9</sup>) denoting an index number and its corresponding coordinates as you see on your radar. It is guaranteed the coordinates given will result in a unique bottom-most point.

<strong>Output</strong>

Print a sequence of N-1 integers (B), where <em>B<sub>i </sub></em>denotes the index of the villain he fends off in the <em>i<sup>th </sup></em>instant (in counter-clockwise direction). Figure for sample testcase-1 is given below.

input 16

12 -3 -1

15 5 5

<ul>

 <li>2 -3</li>

 <li>3 5</li>

 <li>11 2</li>

 <li>-1 4</li>

</ul>

10 -2 2

5 7 4

4 9 3

7 -3 1

6 -3 0

<ul>

 <li>10 -4</li>

 <li>-1 2</li>

</ul>

16 1 4

3 4 -3

11 0 3

output

1 4 5 15 14 16 2 11 9 10 7 6 12 3 13

<ol>

 <li><strong> Cube-Root</strong></li>

</ol>

In this problem, you need to find the integral part of the cube-root of a given integer without using any inbuilt math functions. Further, your solution must run in o(N) time.

<strong>Input</strong>

The only line of input contains a single integer N (−10<sup>9 </sup>≤ N ≤ 10<sup>9</sup>) for which the cube-root has to be computed.

<strong>Output</strong>

Print a single integer X denoting the integral part of the cube-root of the given integer N.

input -125

output -5

input 2348247

output 132

input -617491

output -85