Add your answers to the Algorithms exercises here.

 a)  a = 0
    while (a < n * n * n):
      a = a + n * n

 
    c1 = 1
    c2 = 1 + n
    c3 = 1


    Answer: This is O(n) complexity because run time incease as n increase.



b)  sum = 0
    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1


    c1 = 1
    c2 = n
    c3 = n
    c4 = n^2
    c5 = n^2
    c6 = n^3
    c7 n ^3
    c8 = 1
    c9 = 1
    c10 = 1


    Answer: This is O(n^3) complexity because each loop runs n times except the last loop.


c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0
      return 2 + bunnyEars(bunnies-1)


    c1 = 1
    c2 = 1 + n


    Answer: This is O(n) complexity because run time incease as n increase.

## Exercise II

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.

Well, I assumed the floors are sorted and will do a binary search to determine the value of the middle floor to determin the break point f.

def searchFloors(floors, elem):

  first = 0
  last = len(floors)-1
  
  found = False

  while first <= last and not found:

    middle = (first + last)/2

    if floors[middle] == elem:
      found == True
    else:
      if elem < floors[middle]:
        last = middle-1
        else:
          first = middle +1

    return found

    The run time of this algorithm is 0(n).

