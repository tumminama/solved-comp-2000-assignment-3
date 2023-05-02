Download Link: https://assignmentchef.com/product/solved-comp-2000-assignment-3
<br>
Write the following complete C (or C++) programs.

<ol>

 <li><strong>1</strong>. <strong>c</strong> to implement Floyd’s algorithm to solve the all-pairs shortest-paths problem, where the directed weighted connected graph has no negative-length cycle. [40 marks] <strong>2</strong>. <strong>Dijkstra.c</strong> to implement Dijkstra’s algorithm to solve the single-source shortest-paths problem, where the directed weighted connected graph has no negative weight. <strong>3</strong>. <strong>BellmanFord.c</strong> to implement Bellman and Ford’s algorithm to solve the single-source shortest-paths problem, where the directed weighted connected graph has no negative-length cycle. [30 marks]</li>

</ol>

<ul>

 <li>A graph is represented using an adjacency matrix (also called weight, cost, or length matrix).</li>

 <li>For the <strong>c</strong> program, you may use the following graph to test your program.</li>

 <li>The weight (cost, length) adjacency matrix of the graph is</li>

</ul>




<table width="0">

 <tbody>

  <tr>

   <td width="30"> </td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td rowspan="4" width="198"> </td>

   <td width="30"> </td>

   <td width="30">0</td>

   <td width="30">1</td>

   <td width="30">2</td>

  </tr>

  <tr>

   <td width="30">1</td>

   <td width="30">0</td>

   <td width="30">4</td>

   <td width="30">11</td>

   <td width="30">0</td>

   <td width="30">0</td>

   <td width="30">4</td>

   <td width="30">11</td>

  </tr>

  <tr>

   <td width="30">2</td>

   <td width="30">6</td>

   <td width="30">0</td>

   <td width="30">2</td>

   <td width="30">1</td>

   <td width="30">6</td>

   <td width="30">0</td>

   <td width="30">2</td>

  </tr>

  <tr>

   <td width="30">3</td>

   <td width="30">3</td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td width="30"></td>

   <td width="30">0</td>

  </tr>

 </tbody>

</table>

Given weight adjacency matrix                     Weight adjacency matrix stored in memory

<h4>(I = 99999 indicates )</h4>

A demonstrative output of the <strong>Floyd.c</strong> program is given below.

<h1>The weight matrix W is</h1>

0  4 11

6  0  2

3  I  0

D(1) is

0  4 11

6  0  2

3  7  0

D(2) is

0  4  6

6  0  2

3  7  0

D(3) is

0  4  6

5  0  2

3  7  0

The distance matrix D is

0  4  6

5  0  2

3  7  0

The Path matrix is

<h2> -1 -1  1</h2>

2 -1 -1

-1  0 -1




Path length =   4, Path from 1 to 2 is: 1 –&gt; 2

Path length =   6, Path from 1 to 3 is: 1 –&gt; 2 –&gt; 3

Path length =   5, Path from 2 to 1 is: 2 –&gt; 3 –&gt; 1

Path length =   2, Path from 2 to 3 is: 2 –&gt; 3

Path length =   3, Path from 3 to 1 is: 3 –&gt; 1

Path length =   7, Path from 3 to 2 is: 3 –&gt; 1 –&gt; 2




<ul>

 <li>For the <strong>c</strong> program, you may use the following graph to test your program.</li>

</ul>






















<ul>

 <li>The cost (weight, length) adjacency matrix of the graph is</li>

</ul>




<table width="0">

 <tbody>

  <tr>

   <td width="183">


    <table width="0">

     <tbody>

      <tr>

       <td width="30"> </td>

       <td width="30"><em>v</em><sub>0</sub></td>

       <td width="30"><em>v</em><sub>1</sub></td>

       <td width="30"><em>v</em><sub>2</sub></td>

       <td width="30"><em>v</em><sub>3</sub></td>

       <td width="30"><em>v</em><sub>4</sub></td>

      </tr>

      <tr>

       <td width="30"><em>v</em><sub>0</sub></td>

       <td width="30">0</td>

       <td width="30"></td>

       <td width="30"></td>

       <td width="30">7</td>

       <td width="30"></td>

      </tr>

      <tr>

       <td width="30"><em>v</em><sub>1</sub></td>

       <td width="30">3</td>

       <td width="30">0</td>

       <td width="30">4</td>

       <td width="30"></td>

       <td width="30"></td>

      </tr>

      <tr>

       <td width="30"><em>v</em><sub>2</sub></td>

       <td width="30"></td>

       <td width="30"></td>

       <td width="30">0</td>

       <td width="30"></td>

       <td width="30">6</td>

      </tr>

      <tr>

       <td width="30"><em>v</em><sub>3</sub></td>

       <td width="30"></td>

       <td width="30">2</td>

       <td width="30">5</td>

       <td width="30">0</td>

       <td width="30"></td>

      </tr>

      <tr>

       <td width="30"><em>v</em><sub>4</sub></td>

       <td width="30"></td>

       <td width="30"></td>

       <td width="30"></td>

       <td width="30">4</td>

       <td width="30">0</td>

      </tr>

     </tbody>

    </table></td>

   <td width="659">


    <table width="0">

     <tbody>

      <tr>

       <td width="30"> </td>

       <td width="30">0</td>

       <td width="30">1</td>

       <td width="30">2</td>

       <td width="30">3</td>

       <td width="30">4</td>

      </tr>

      <tr>

       <td width="30">0</td>

       <td width="30">0</td>

       <td width="30">I</td>

       <td width="30">I</td>

       <td width="30">7</td>

       <td width="30">I</td>

      </tr>

      <tr>

       <td width="30">1</td>

       <td width="30">3</td>

       <td width="30">0</td>

       <td width="30">4</td>

       <td width="30">I</td>

       <td width="30">I</td>

      </tr>

      <tr>

       <td width="30">2</td>

       <td width="30">I</td>

       <td width="30">I</td>

       <td width="30">0</td>

       <td width="30">I</td>

       <td width="30">6</td>

      </tr>

      <tr>

       <td width="30">3</td>

       <td width="30">I</td>

       <td width="30">2</td>

       <td width="30">5</td>

       <td width="30">0</td>

       <td width="30">I</td>

      </tr>

      <tr>

       <td width="30">4</td>

       <td width="30">I</td>

       <td width="30">I</td>

       <td width="30">I</td>

       <td width="30">4</td>

       <td width="30">0</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

Given cost adjacency matrix                         Cost adjacency matrix stored in memory

<h4>(I = 99999 indicates )</h4>




A demonstrative output of the <strong>Dijkstra.c</strong> program is given below.




The weight matrix W is

0     I     I     7     I

3     0     4     I     I

I     I     0     I     6

I     2     5     0     I

I     I     I     4     0

<ol>

 <li>dist[] and parent[] are

  <ul>

   <li>I I     7     I</li>

   <li>-1 -1     0    -1</li>

  </ul></li>

 <li>dist[] and parent[] are

  <ul>

   <li>9   12     7     I</li>

   <li>3 3     0    -1</li>

  </ul></li>

 <li>dist[] and parent[] are

  <ul>

   <li>9 12     7     I</li>

   <li>3 3     0    -1</li>

  </ul></li>

 <li>dist[] and parent[] are

  <ul>

   <li>9 12     7    18</li>

  </ul></li>

</ol>

<h2>    -1     3     3     0     2</h2>

The distance array dist[] is

0     9    12     7    18

The parent array parent[] is

<h2>    -1     3     3     0     2</h2>




Path length =   9, Path from 0 to 1 is: 0 –&gt; 3 –&gt; 1

Path length =  12, Path from 0 to 2 is: 0 –&gt; 3 –&gt; 2

Path length =   7, Path from 0 to 3 is: 0 –&gt; 3 Path length =  18, Path from 0 to 4 is: 0 –&gt; 3 –&gt; 2 –&gt; 4



















<ul>

 <li>For the <strong>c</strong> program, you may use the following graph to test your program.</li>

</ul>







<ul>

 <li>The cost (weight, length) adjacency matrix of the graph is</li>

</ul>




<table width="0">

 <tbody>

  <tr>

   <td width="30"> </td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td width="30">4</td>

   <td width="30">5</td>

   <td width="30">6</td>

   <td rowspan="7" width="107"> </td>

   <td width="30"> </td>

   <td width="30">0</td>

   <td width="30">1</td>

   <td width="30">2</td>

   <td width="30">3</td>

   <td width="30">4</td>

   <td width="30">5</td>

  </tr>

  <tr>

   <td width="30">1</td>

   <td width="30">0</td>

   <td width="30">2</td>

   <td width="30">4</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">0</td>

   <td width="30">2</td>

   <td width="30">4</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

  </tr>

  <tr>

   <td width="30">2</td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">-3</td>

   <td width="30">1</td>

   <td width="30">5</td>

   <td width="30"></td>

   <td width="30">1</td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">-3</td>

   <td width="30">1</td>

   <td width="30">5</td>

   <td width="30"></td>

  </tr>

  <tr>

   <td width="30">3</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">-4</td>

   <td width="30">-2</td>

   <td width="30"></td>

   <td width="30">2</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">-4</td>

   <td width="30">-2</td>

   <td width="30"></td>

  </tr>

  <tr>

   <td width="30">4</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30"></td>

   <td width="30">8</td>

   <td width="30">3</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30"></td>

   <td width="30">8</td>

  </tr>

  <tr>

   <td width="30">5</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">4</td>

   <td width="30">0</td>

   <td width="30">6</td>

   <td width="30">4</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">4</td>

   <td width="30">0</td>

   <td width="30">6</td>

  </tr>

  <tr>

   <td width="30">6</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

   <td width="30">5</td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30"></td>

   <td width="30">0</td>

  </tr>

 </tbody>

</table>

Given cost adjacency matrix                         Cost adjacency matrix stored in memory

<h4>(I = 99999 indicates )</h4>




A demonstrative output of the <strong>BellmanFord.c</strong> program is given below.




The weight matrix W is

0  2  4  I  I  I

I  0 -3  1  5  I

I  I  0 -4 -2  I

I  I  I  0  I  8

I  I  I  4  0  6    I  I  I  I  I  0 dist(1) is    0  2  4  I  I  I   -1  1  1 -1 -1 -1 dist(2) is    0  2 -1  0  2  I   -1  1  2  3  3 -1 dist(3) is    0  2 -1 -5 -3  8   -1  1  2  3  3  4

dist(4) is

0  2 -1 -5 -3  3

-1  1  2  3  3  4

dist(5) is

0  2 -1 -5 -3  3

-1  1  2  3  3  4

The distance array dist is

0  2 -1 -5 -3  3

The parent array is

-1  1  2  3  3  4




Path length = 2, Path from 1 to 2 is: 1 –&gt; 2

Path length = -1, Path from 1 to 3 is: 1 –&gt; 2 –&gt; 3

Path length = -5, Path from 1 to 4 is: 1 –&gt; 2 –&gt; 3 –&gt; 4

Path length = -3, Path from 1 to 5 is: 1 –&gt; 2 –&gt; 3 –&gt; 5

Path length = 3, Path from 1 to 6 is: 1 –&gt; 2 –&gt; 3 –&gt; 4 –&gt; 6