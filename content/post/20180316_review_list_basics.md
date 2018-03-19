+++
title = "Homework - Review List Basics"
draft = true
date = "2018-03-16"
Tags = ["list"]
Categories = ["homework"]
+++
I taught Ethan the concept of list in Python two weeks ago and showed him all list API provided, such as append/insert/remove/pop/[]/index. He has some basic understanding list as a collection of items that makes sense to be collected together; but still have difficulties to proficiently use it and its APIs. For example, I have showed him the [] operator many times as the way to access the element in the list. But he was still confused with index function when he wrote code to access list. Also when he meets the situation that if statement is used to decide add or not add element to a list, he seems more adapted to the idea that adding all elements and then remove some elements gradually.

So I made up a simple quiz mostly about basic list operations as following.

```
For the number between 1 and 100, group numbers to 2 lists
- List1 where elements can be divided by 2
- List2 where elements can be divided by 3
* Find the length of List1 and List2
* Find the sum of List1 and List2
* Find the element in List1 that are also in List2
* Find the element in List1 that are not in List2
```

{{< highlight python "linenos=inline,hl_lines=1 2">}}
list1 = []
list2 = []

for k in range(1, 101):
    if k%2==0:
        list1.append(k)
    if k%3==0:
        list2.append(k)

print(list1)
print(list2)

print(len(list1))
print(len(list2))

print(sum(list1))
print(sum(list2))

list3 = []
for l in list1:
    if l in list2:
        list3.append(l)

list4 = []
for l1 in list1:
    if l1 not in list2:
        list4.append(l1)

print(list3)
print(list4)
{{< /highlight >}}
```Python

```
