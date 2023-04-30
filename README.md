Download Link: https://assignmentchef.com/product/solved-cs300-homework-4-binary-heap
<br>
In this homework, you will write a program that finds and maintains the median of streaming integers. Your program must store all integers as well as updating the median value as new inputs arrive. To achieve both goals, your program must make use of the Heap data structure in the background. The program will utilize two heaps: a <strong>MaxHeap</strong>​ and a <strong>MinHeap</strong>​ ​. Each streamed integer will be stored in the appropriate Heap in<strong> O(logN). </strong>Using​ the capabilities of the heap data structure, the program tells the median in <strong>O(1)</strong>​ time complexity.​

Therefore, you have to provide a Heap implementation which is used as both<strong> MaxHeap</strong> and <strong>MinHeap</strong>​     in the program flow.

Note that this an implementation of Question 11 of Recitation 5.

<strong> </strong>

<strong>Program Flow</strong>

Streaming integers will be read from <strong>.txt</strong>​ files. Each integer at each file will be considered as the next integer in the stream. Therefore you are going to get a name of a file from the console until <strong>Ctrl</strong>​<strong> + Z</strong> is pressed, which ends the input (HINT: You may use <strong>getline(cin,</strong>​<strong> fileName)</strong>).​ After getting the name of each file, you have to open the input file and process all the integers in it. The files will contain only signed integers and you do not have to do input checks. Please check sample runs and sample input files. After processing each file, you have to prompt the current median.

<strong>Insertions: </strong>

As mentioned before, your program has to run a <strong>MaxHeap</strong>​ and a <strong>MinHeap.</strong>​ Depending​ on the current value of <strong>median</strong>​ ,​ you will insert the next integer either to the <strong>MaxHeap</strong>​ or the <strong>MinHeap.</strong>​ Particularly,​ <strong>MaxHeap </strong>is​ responsible for storing the integers less than the <strong>median</strong>​ ,​ and <strong>MinHeap</strong>​ stores​ the integers greater than the <strong>median.</strong>​ Therefore, new insertions will be made in this fashion.​          <strong>Telling the Median: </strong>

If the number of elements in both Heaps are equal, the median is the average of the top elements of the <strong>MaxHeap </strong>and​<strong> MinHeap.</strong> Otherwise, it is equal to the top element of the one which has more elements. Note that the difference in the number of elements between the heaps is either 1 or 0. Also note that the top element refers to the maximum element for <strong>MaxHeap</strong>​ and the minimum element for <strong>MinHeap,</strong>​ which can be decided at O(1).










<strong>Rules: </strong>

<ul>

 <li>You have to use Heaps, no other data structure or sorting methods are allowed.</li>

 <li>You can’t give separate implementations for <strong>MaxHeap</strong>​ and ​      <strong>MinHeap</strong>​             . Code duplications will​ lose points. You have to create a class hierarchy and use polymorphism or use function pointers.</li>

 <li>Heap implementation must be template.</li>

</ul>




<strong>Input: </strong>

The file names will be received from the console until the input is ended by the user.

<strong>Output: </strong>

After processing each file, you need to print out the current median.




<strong>Sample Run 1: </strong>

Please enter the next filename that contains integer stream: ​input1<u>.</u>txt current median: 520

Please enter the next filename that contains integer stream: ​input2<u>.</u>txt current median: 487

Please enter the next filename that contains integer stream: ​input3<u>.</u>txt current median: 481

Please enter the next filename that contains integer stream: ​input4<u>.</u>txt current median: 434.5

Please enter the next filename that contains integer stream: ​Ctrl<span style="text-decoration: line-through;">–</span>Z Press