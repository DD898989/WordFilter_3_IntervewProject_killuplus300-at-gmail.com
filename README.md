# http-WordFilter_3_IntervewProject_killuplus300-at-gmail.com
<br/>
<br/>
<br/>

Dictionary Tree
--
![](https://github.com/DD898989/Pictures/blob/master/1107%202333.PNG)<br/>
##### from Kelvin Lau   https://www.raywenderlich.com/1053-swift-algorithm-club-swift-tree-data-structure
<br/>
<br/>
<br/>

Fast Way To Make Balanced Binary Tree
--
![](https://github.com/DD898989/Pictures/blob/master/1107%20003.PNG)<br/>
<br/>
<br/>
<br/>

Not Handle String Itself, Handle The Array
--
`wstring input = L” A long, long time ago in a land far away”;`<br/>
`int* ptr_input = new int[Input.size()]();`<br/>

Advantage:<br/>
1. Array can be handled by many threads in the same time.<br/>
2. Better word filter:<br/>
  
wstring input            =     L”disagree”; <br/>
(replace “agree”      ->)   L”dis****”;<br/>
(replace “disagree” ->)   L”dis****”;<br/>
  
wstring input           =      L”disagree”; <br/>
(mark “agree”          ->)   L”dis[agree](#)”;<br/>
(mark “disagree”     ->)   L”[disagree](#)”;<br/>
(replace mark          ->)    L”*******”;<br/>
<br/>
<br/>
<br/>

Search Logic
--
### 7 Chars Searcher

![](https://github.com/DD898989/Pictures/blob/master/7.png)<br/>

### 3 Chars Searcher

![](https://github.com/DD898989/Pictures/blob/master/3.png)<br/>
<br/>
<br/>
<br/>

Run Length Encoding
--
![](https://github.com/DD898989/Pictures/blob/master/1107%202348.PNG)<br/>
####Replacing from behind make output correct
<br/>
<br/>
<br/>

Insert All Possible Case Form Than Skip Comparing Case In Function
--
`BST.Insert(L”APPLE”);`<br/>
`BST.Insert(L”apple”);`<br/>
`BST.Insert(L”Apple”);`<br/>
`int strcasecmp(wchar_t *s1, wchar_t *s2)` <br/> 
`{  `<br/>
`	int c1, c2;  `<br/>
`	do {  `<br/>
`		c1 = *s1++; //tolower(*s1++);`<br/>
`		c2 = *s2++; //tolower(*s2++);`<br/>
`	} while(c1 == c2 && c1 != 0); `<br/>
`	return c1 - c2;  `<br/>
`} `<br/>

<br/>
<br/>
<br/>

Analysis
--
##### filter cases　: 18500
##### x-axis　　　: input length(chars)
##### y-axis　　　: average finish time(second)
![](https://github.com/DD898989/Pictures/blob/master/1107%20001.PNG)<br/>
time ∝ input length<br/>
<br/>
<br/>
<br/>
<br/>
##### input length: 1000
##### x-axis　　　: filter cases
##### y-axis　　　: average finish time(second)
![](https://github.com/DD898989/Pictures/blob/master/1107%20002.PNG)<br/>
test cases does's seem to have relation with time<br/>
in this algorithm, we mark an number on the location where match case, 
so the more cases means less operation in later time,
since the test cases is an dictionary, this is a reasonable result<br/>
<br/>
<br/>
<br/>
### Time Complexity:
#### O(N)
Let N = Input length<br/>
filter cases not relevant in this algorithm<br/>
