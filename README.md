Download Link: https://assignmentchef.com/product/solved-data-structures-and-algorithms-cs-f211-lab-sheet-7
<br>
<ol>

 <li>Alice and Bob are playing the tag game. The game should be played on an undirected rooted tree of <strong><em>n</em></strong> vertices. Vertex 1 is the root of the tree. Alice starts at vertex 1 and Bob starts at vertex <strong><em>x</em></strong> (<strong><em>x</em></strong> ≠ 1). The moves are made in turns, Bob goes first. In one move, one can either stay at the current vertex or travel to a neighbouring one. The game ends when Alice reaches the same vertex where Bob is standing. Alice wants to minimize the total number of moves and Bob wants to maximize it. Determine how many moves the game will last.</li>

</ol>




<strong>Input: </strong>

The first line contains two integer numbers <strong><em>n</em></strong> and <strong><em>x</em></strong>.

Each of the next <strong><em>n - 1</em></strong> lines contain two integer numbers <strong><em>a</em></strong> and <strong><em>b</em></strong> (<strong><em>1 ≤ a, b ≤ n</em></strong>) — edges of the tree. It is guaranteed that the edges will form a valid tree.




<strong>Output: </strong>

Print the total number of moves Alice and Bob will make.




<strong>Example: </strong>

<strong>Input: </strong>

4 3

<h1><a name="_Toc13332"></a>1  2</h1>

<h1><a name="_Toc13333"></a>2  3</h1>

2 4

<strong> </strong>

<strong>Output: </strong>

4




<strong>Explanation: </strong>

Bob: stay at vertex 3

Alice: go to vertex 2

Bob: stay at vertex 3

Alice: go to vertex 3




<ol start="2">

 <li>Your city has <strong><em>n</em></strong> junctions. There are <strong><em>m</em></strong> one-way roads between the junctions. As a mayor of the city, you have to ensure the security of all the junctions. To ensure the security, you have to build some police checkposts. Checkposts can only be built in a junction. A checkpost at junction <strong><em>i</em></strong> can protect junction <strong><em>j</em></strong> if either <strong><em>i = j</em></strong> or the police patrol car can go to <strong><em>j</em></strong> from <strong><em>i</em></strong> and then come back to <strong><em>i</em></strong>. Building checkposts costs some money. As some areas of the city are more expensive than others, building checkposts at some junctions might require more money than other junctions. You have to determine the minimum possible money needed to ensure the security of all the junctions. Also, you have to find the number of ways in which security can be ensured in minimum price and also using minimum number of checkposts. Two ways are different if any of the junctions contains a checkpost in one of them and do not contain in the other.</li>

</ol>




<strong>Input: </strong>

In the first line, you will be given an integer <strong><em>n</em></strong>, number of junctions.

In the next line, <strong><em>n</em></strong> space-separated integers will be given. The <strong><em>i</em></strong><sup>th</sup> integer is the cost of building a checkpost at the <strong><em>i</em></strong><sup>th</sup> junction.

The next line will contain an integer <strong><em>m</em></strong>.

Each of the next <strong><em>m</em></strong> lines contains two integers <strong><em>u<sub>i</sub></em></strong> and <strong><em>v<sub>i</sub></em></strong>. A pair <strong><em>u<sub>i</sub>, v<sub>i</sub></em></strong> means, that there is a one-way road which goes from <strong><em>u<sub>i</sub></em></strong> to <strong><em>v<sub>i</sub></em></strong>. There will not be more than one road between two nodes in the same direction.

<strong> </strong>

<strong>Output: </strong>

Print two integers separated by spaces. The first one is the minimum possible money needed to ensure the security of all the junctions. The second one is the number of ways you can ensure the security with the minimum cost.




<strong>Example: </strong>

<strong>Input: </strong>

<h1><a name="_Toc13334"></a>3</h1>

1 2 3

3

<ul>

 <li>2</li>

 <li>3</li>

 <li>2</li>

</ul>

<strong> </strong>

<strong>Output: </strong>

3 1




<ol start="3">

 <li>Let’s consider a rooted undirected tree with <strong><em>n</em></strong> vertices, numbered <strong><em>1</em></strong> through <strong><em>n</em></strong>. There are many ways to represent such a tree. One way is to create an array with <strong><em>n</em></strong> integers <strong><em>p<sub>1</sub></em></strong>, <strong><em>p<sub>2</sub></em></strong>, …, <strong><em>p<sub>n</sub></em></strong> where <strong><em>p<sub>i</sub></em></strong> denotes a parent of vertex <strong><em>i</em></strong> (for convenience a root is considered its own parent). Given a sequence <strong><em>p<sub>1</sub></em></strong>, <strong><em>p<sub>2</sub></em></strong>, …, <strong><em>p<sub>n</sub></em></strong>, one is able to restore a tree subject to the following conditions:</li>

</ol>




<ol>

 <li>There must be exactly one index <strong><em>r</em></strong> such that <strong><em>p<sub>r</sub></em></strong> = <strong><em>r</em></strong>. A vertex <strong><em>r</em></strong> is a root of the tree.</li>

 <li>For all other <strong><em>n - 1</em></strong> vertices, for every vertex <strong><em>i</em></strong>, there is an edge between vertex <strong><em>i</em></strong> and vertex <strong><em>p<sub>i</sub></em></strong>.</li>

</ol>




A sequence <strong><em>p<sub>1</sub></em></strong>, <strong><em>p<sub>2</sub></em></strong>, …, <strong><em>p<sub>n</sub></em></strong> is called valid if the described procedure generates some (any) rooted tree. For example, for <strong><em>n</em></strong> = 3 sequences (1, 2, 2), (2, 3, 1) and (2, 1, 3) are not valid.

You are given a sequence <strong><em>a<sub>1</sub>, a<sub>2</sub> , …, a<sub>n</sub></em></strong>  not necessarily valid. Your task is to change the minimum number of elements, in order to get a valid sequence using only the vertices from <strong><em>1</em></strong> to <strong><em>n</em></strong>. Print the minimum number of changes and an example of a valid sequence after that number of changes. If there are more than one valid sequence achievable in the minimum number of changes, print any one of them.




<strong>Input: </strong>

The first line of the input contains an integer <strong><em>n</em></strong> — the number of vertices in the tree. The second line contains <strong><em>n</em></strong> integers <strong><em>a<sub>1</sub>, a<sub>2</sub> , …, a<sub>n</sub></em></strong>.




<strong>Output: </strong>

In the first line, print the minimum number of elements to be changed, in order to get a valid sequence. In the second line, print any valid sequence possible to get from <strong><em>a<sub>1</sub>, a<sub>2</sub> , …, a<sub>n</sub></em></strong> in the minimum number of changes. If there are many such sequences, any of them is acceptab;e.

<strong> </strong>

<strong>Example: </strong>

<strong>Input: </strong>

<h1><a name="_Toc13335"></a>4</h1>

2 3 3 4

<strong>Output: </strong>

1

2 3 4 4




<strong>Comment:</strong> Note that 4 3 3 2 is also a valid tree, however, you end up changing two elements instead of one.




<ol start="4">

 <li>You came to an exhibition and one exhibit has drawn your attention. It consists of <strong><em>n</em></strong> stacks of blocks, where the <strong><em>i</em></strong><sup>th</sup> stack consists of <strong><em>a<sub>i</sub></em></strong> blocks resting on the surface. The height of the exhibit is equal to <strong><em>m</em></strong>. Consequently, the number of blocks in each stack is less than or equal to <strong><em>m</em></strong>. There is a camera on the ceiling that sees the top view of the blocks and a camera on the right wall that sees the side view of the blocks. Find the maximum number of blocks you can remove such that the views for both the cameras do not change. Note, that while originally all blocks are stacked on the floor, it is not required for them to stay connected to the floor after some blocks are removed. There is no gravity in the whole exhibition, so no block will fall down, even if the block underneath is removed. <strong><u>It not allowed to move blocks from one stack to another, i.e., you are not</u> <u>allowed to move blocks across the stacks in order to preserve both the views.</u></strong></li>

</ol>




<strong>Input:  </strong>

The first line contains two integers <strong><em>n</em></strong> and <strong><em>m</em></strong>— the number of stacks and the height of the exhibit.

The second line contains <strong><em>n</em></strong> integers <strong>a<sub>1</sub>, a<sub>2</sub>, … ,a<sub>n</sub></strong>— the number of blocks in each stack from left to right.

<strong> </strong>

<strong>Output: </strong>

Print exactly one integer — the maximum number of blocks that can be removed without changing the views.

<strong> </strong>

<strong>Example1: </strong>

<strong>Input: </strong>

5 6

3 3 3 3 3




<table width="30">

 <tbody>

  <tr>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="30"> </td>

  </tr>

 </tbody>

</table>

<table width="168">

 <tbody>

  <tr>

   <td colspan="5" width="168"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

 </tbody>

</table>

<table width="168">

 <tbody>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

 </tbody>

</table>

<strong>Top View </strong>

<strong>Side View <em>m </em></strong>




<strong>Output:</strong>

10

<table width="168">

 <tbody>

  <tr>

   <td colspan="5" width="168"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

  <tr>

   <td width="36"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

   <td width="36"> </td>

   <td width="30"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Explanation: </strong>

Here, total 10 blocks have been removed. As shown in the figure above, even after removal, from the side, 3 blocks can be seen and from the top, 5 blocks can be seen. The top camera does not care whether the 5 blocks are at the same height or not. Similarly, the side camera does not care whether the 3 blocks belong to the same stack or not.




<strong>Example 2: </strong>

<strong>Input: </strong>

3 5

1 2 4




<strong>Output: </strong>3

<ol start="5">

 <li>You live in a town with <strong><em>n</em></strong> junctions and <strong><em>m</em></strong> bi-directional roads. Each road connects two distinct junctions and no two roads connect the same pair of junctions. It is possible to go from any junction to any other junction by these roads. The distance between two junctions is equal to the minimum possible number of roads on a path between them. Your city mayor wants to build a new road in such a way that the distance between the junctions <strong><em>s</em></strong> and <strong><em>t</em></strong> will not decrease. You are assigned a task to compute the number of pairs of junctions that are not connected by the road, such that if the new road between these two junctions is built the distance between <strong><em>s</em></strong> and <strong><em>t</em></strong> won’t decrease.</li>

</ol>




<strong>Input: </strong>

The first line of the input contains integers <strong><em>n</em></strong>, <strong><em>m</em></strong>, <strong><em>s</em></strong> and <strong><em>t</em></strong> — the number of junctions and the number of roads, as well as the indices of junctions <strong><em>s</em></strong> and <strong><em>t</em></strong>.

The <strong><em>i</em></strong><sup>th</sup> of the following <strong><em>m</em></strong> lines contains two integers, <strong><em>u<sub>i</sub></em></strong> and <strong><em>v<sub>i</sub></em></strong>, meaning that this road connects junctions <strong><em>u<sub>i</sub></em></strong> and <strong><em>v<sub>i</sub></em></strong> directly.

<strong> </strong>

<strong>Output: </strong>

Print one integer — the number of pairs of junctions not connected by a direct road, such that building a road between these two junctions won’t decrease the distance between junctions <strong><em>s</em></strong> and <strong><em>t</em></strong>.




<strong>Example1: Input: </strong>

5 4 1 5

<a href="#_Toc13332">1                                                                                                                                                                          2 </a>

<a href="#_Toc13333">2                                                                                                                                                                          3 </a>

<a href="#_Toc13334">3                                                                                                                                                                          4 </a>

<a href="#_Toc13335">4                                                                                                                                                                          5 </a>







<strong>Output: </strong>

0




<strong>Explanation:  </strong>

The pairs of junctions which are not connected by a direct road are: (1, 3), (1, 4), (1, 5), (2, 4), (2, 5) and (3, 5). If you build any road between any one of these city pairs, then the distance between 3 and 5 will reduce. That is why, no road can be built.

<strong> </strong>

<strong>Example 2: Input: </strong>

5 4 3 5

<ul>

 <li>2</li>

 <li>3</li>

 <li>4</li>

 <li>5</li>

</ul>




<strong>Output: </strong>

5




<strong>Explanation: </strong>

The pairs of junctions which are not connected by a direct road are: (1, 3), (1, 4), (1, 5), (2, 4), (2, 5) and (3,

5). Out of these, if you build roads between (1, 3), (1, 4), (1, 5), (2, 4) and (2, 5), then the distance between 3 and 5 will not reduce. That is why, the answer is 5.




<ol start="6">

 <li>Luka Doncic is a big fan of substring. His mentor Dirk knows that and decided to challenge him for that. He gave him a number <strong><em>n</em></strong> and a set of characters <strong><em>P</em></strong>. Size of <strong><em>P</em></strong> is <strong><em>k</em></strong>. Find a string <strong><em>S</em></strong> such that every possible string that can be constructed from the characters of <strong><em>P</em></strong>, each having length <strong><em>n</em></strong> appears exactly once as a substring in <strong><em>S</em></strong>. You have to do this in O(<strong><em>k<sup>n</sup></em></strong>) time.</li>

</ol>




<strong>Input: <em>n k </em></strong>

Array of size <strong><em>k</em></strong>




<strong>Example: </strong>

<strong>Input: </strong>

3 2

0 1




<strong>Output: </strong>

0011101000




<strong>Example: </strong>

<strong>Input:  </strong>

2 2

0 1




<strong>Output: </strong>

01100




<ol start="7">

 <li>You have to the count number of crossovers while sorting a set of unsorted elements.</li>

</ol>




<strong>Input: </strong>

The elements to be sorted




<strong>Output: </strong>

The number of crossovers required to sort the array.




<strong>Example: </strong>

<strong>Input</strong>:

3 2 1 4 5

<strong>Output</strong>: 3




<strong>Explanation:</strong>

<strong>Before Sorting:</strong>                        3 2 1 4 5

 | /  | |

|/   | |

/ |   | | <strong>After sorting:</strong>                           1 2 3 4 5

line (1 to 1) crosses line (2 to 2) line (1 to 1) crosses line (3 to 3) line (2 to 2) crosses line (3 to 3)




<ol start="8">

 <li>Naruto is now participating in Chunin Exams. He needs to solve a riddle to get a secret weapon. He is given a number <strong><em>n</em></strong> and he needs to find a set of numbers that are smaller than <strong><em>n</em></strong> but follow an <em>adjacent_one</em> condition<em>. adjacent_one</em> condition is fulfilled if all the digits in the number differ from their respective adjacent digits by 1. For example, 456 follows <em>adjacent_one</em> condition but 782 doesn’t.</li>

</ol>




<strong>Note:</strong> All single digit numbers fulfill <em>adjacent_one</em> condition.

<strong>Note:</strong> Difference between 9 and 0 is not 1.




<strong>Input: </strong>

<strong><em>n </em></strong>




<strong>Output: </strong>

The set of numbers satisfying the condition




<strong>Example 1: </strong>

<strong>Input: </strong>

20




<strong>Output: </strong>

0 1 2 3 4 5 6 7 8 9 10 12




<strong>Example 2: </strong>

<strong>Input:  </strong>

105




<strong>Output: </strong>

0 1 2 3 4 5 6 7 8 9 10 12 21 23 32 34 43 45 54 56 65 67 76 78 87 89 98 101




<ol start="9">

 <li>Mohit is a traveller. He travels all around the world collecting non-negative numbers. After completing all of his journeys, he decides to form the largest number from the list of numbers. Help Mohit to fulfil his quest.</li>

</ol>




<strong>Input: </strong>

The first line contains the total number of non-negative numbers collected. The second line contains the non-negative numbers.




<strong>Output: </strong>

The largest number.




<strong>Example: </strong>

<strong>Input: </strong>

5

3 30 34 5 9




<strong>Output: </strong>

9534330







****************************





