# technical-interview-preparation

## 👨‍💻 About Repo
In this repository, I am following the NeetCode 150 problems. For each problem, I added a brief explanation and include a link to the solution I created in LeetCode. This is an effort to continue practicing for technical interviews and continue problem solving!

|Pattern                                             |Problem                             |Explanation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |Leetcode                                                                                                              |
|----------------------------------------------------|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
|Array & Hashing                                     |Contains Duplicate                  |Use a HashTable. It will track the values that we have seen already. If a value from the array appears again, then we know it is a duplicate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |https://leetcode.com/problems/contains-duplicate/solutions/3297167/javascript-easy-solution-using-an-object/          |
|Array & Hashing                                     |Valid Anagram                       |Use a Hash Table. The hash table will contain the frequencies that appear on string s. Then we loop through string t and check if it exists in the hash table, if does not or it is zero then it is not an anagram.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |https://leetcode.com/problems/valid-anagram/solutions/3301839/javascript-solution-with-hash-table/                    |
|Array & Hashing                                     |Two Sum                             |- There is only one solution. - Use hash table to store visited values from array {num:index}. - Then we subtract target - num, we check if the result exists in the map. If it does we found our pair. If not we add visited pair into the map                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |https://leetcode.com/problems/two-sum/description/                                                                    |
|Two Pointers                                        |Valid Palindrome                    |Use Two pointers and a isAlphanumeric function to determine if character is isAlpha or not                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |https://leetcode.com/problems/valid-palindrome/solutions/3308520/javascript-two-pointers/                             |
|Two Pointers (On neetcode it said sliding window...)|Best Time to Buy and Sell Stock     |Use Two pointers (l for buy price and r for sell price). We iterate the array in search of a buy price and sell price                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |https://leetcode.com/problems/best-time-to-buy-and-sell-stock/solutions/3329759/javascript-two-pointer-solution/      |
|Stack                                               |Valid Parenthesis                   |use stack (array), push the opening tags into the array. As you are iterating and you find closing tag, then compare to see if they properly close. if they do not close then return false                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |https://leetcode.com/problems/valid-parentheses/solutions/3363438/javascript-easy-to-understand-stack-approach/       |
|Binary Search                                       |Binary Search                       |use Three pointers (left, middle, right) to cut down the search in half. You will need to use a while with condition L <= R so that when the L passes the R you stop the loop. Also remember that you need to update the m index position by either l = m + 1 or r = m - 1                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |https://leetcode.com/problems/binary-search/solutions/4036905/three-pointers-javascript-solution/                     |
|Linked List                                         |Reverse Linked List                 |use two pointers. A Prev and a Current one. Prev will point to the entire list at the end. Current is to navigate across the list. We will use a temp node which will store the curr.next node to follow. Then we change the pointers. Also iterative solution is better uses Time O(n) Space O(1). Recursion uses Time O(n) Space O(n)                                                                                                                                                                                                                                                                                                                                                                                                          |https://leetcode.com/problems/reverse-linked-list/solutions/4041591/two-pointers-iterative-javascript-solution/       |
|Linked List                                         |Merge Two Sorted Lists              |Use a temp node new ListNode(0) to place the nodes that we will compare in list1 and list2. Then create a result node that points to temp node (result node will point to the sorted list). Then you check for the values of list1 and list2 and compare them list1Val > list2Val (then push list2 value to temp.next and move list2 to the next value), list1Val < list2Val (then push list1 value to temp.next and move list1 to the next value), and list1Val === list2Val (then push list1 value to temp.next and move list1 to the next value).              Dont forget to check if either one reach null first! If either one reaches first then just append the remaining nodes to it. list1 == null, then temp.next = list2 (vise versa)|https://leetcode.com/problems/merge-two-sorted-lists/solutions/4045404/merge-sorted-list-javascript-solution/         |
|Trees                                               |Invert Binary Tree                  |Use Depth - First Search. For every node that we visit, we check the left and right nodes and swap their positions                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |https://leetcode.com/problems/invert-binary-tree/solutions/4049268/javascript-depth-first-search-solution/            |
|Trees                                               |Maximum Depth of Binary Tree        |Use DFS with recursion. Use Math.max to help determine which subtree has a bigger depth                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |https://leetcode.com/problems/maximum-depth-of-binary-tree/solutions/4049499/depth-first-search-recursion-javascript/ |
|Trees                                               |Diameter of Binary Tree             |Use DFS. We need to find the height 1 + Math.max(leftHeight, rightHeight); and the diameter Math.max(diameter[0], 2 + leftHeight + rightHeight); We apply dfs on the left and right side of each node. The base case when it reaches until null it will return a -1                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |https://leetcode.com/problems/diameter-of-binary-tree/solutions/4078550/javascript-depth-first-search/                |
|Trees                                               |Balanced Binary Tree                |Use DFS recursively. Go down until you reach a leaf node and when you reach a leaf node return [true, 0] where true is if it balanced and 0 is the height. You do this for both left and right sides. And check if it is balanced by using the array item 0. Use Math.max(leftTree[1], rightTree[1]) to determine height of the tree                                                                                                                                                                                                                                                                                                                                                                                                             |https://leetcode.com/problems/balanced-binary-tree/solutions/4097474/javascript-solution-recursive-depth-first-search/|
|Trees                                               |Same Tree                           |Use DFS Recursively on both tree. Have three bases cases to check the value of each node as your are recursing. Check for either one is null, check for values are not the same then return false. then if both nodes are null, then we return true                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |https://leetcode.com/problems/same-tree/solutions/4102336/javascript-depth-first-search-solution/                     |
|Trees                                               |Subtree of another tree             |Use DFS to go through the nodes of the root tree. You will want to apply the function to the left and right. Then use the isSameTree algorithm to help you compare the two trees and see if they are the same                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |https://leetcode.com/problems/subtree-of-another-tree/solutions/4127122/javascript-depth-first-search-solution/       |
|Heaps                                               |703. Kth Largest Element in a Stream|use a heap!                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |https://leetcode.com/problems/kth-largest-element-in-a-stream/solutions/4232488/python3-min-heap-solution/            |
