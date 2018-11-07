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

Run Length Encoding
--
https://github.com/DD898989/Pictures/blob/master/11072342.PNG
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

`wstring input            =     L”disagree”;` <br/>
(replace “agree”      ->)`   L”dis****”;`<br/>
(replace “disagree” ->)`   L”dis****”;`<br/>

`wstring input           =      L”disagree”;` <br/>
(mark “agree”          ->)`   L”disagree”;`<br/>
(mark “disagree”     ->)`   L”disagree”;`<br/>
(replace mark          ->)`    L”*******”;`<br/>
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
