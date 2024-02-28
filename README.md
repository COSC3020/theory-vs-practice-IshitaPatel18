[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1. The asymptotic analysis may be misleading because of the constants that were
     were dropped when solving for the complexity. They actually affect the runtime
     of the algorithm (specific timing), where as the complexity simply explains
     how runtime should look.

  2. The hardware/ different computers the algorithm is being run on can make a
     significant difference because any hardware that is faster and has a greater
     memory capacity will be able to run the algorithm more quickly. For example,
     the Hash Table program from COSC 2030, was run on my laptop in less than one second, but
     when run on the PI's it took approximately 3 seconds because of the lower
     memory capacity. Asymptotically, yes it technically will always look the same, but
     the expected result from the typical asymptotic analysis, or the time that is most accurate
     will change based on the hardware used.
     
  3. The lower order terms that are dropped when calculating the asymptotic complexity
     can also cause the asymptotic analysis to be misleading. For example, when we
     calculated the asymptotic complexity of mergesort, we had that $n + log(n)\in \Theta(log(n))$.
     For our runtime, we would be looking at the log(n), where the n is dropped, but in practice, that n
     makes a huge difference. Another example could be $n^5 + n^4 \in O(n^5)$, where we regard only the $n^5$
     because the $n^4$ in this case is regarded as a lower order term, but in practice, the $n^4$ would cause
     a significant change in the runtime. (I was stuck on another reason and howardthegr8one had this reason
     which I found to be very interesting and something that I didn't realize at first).

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  1. Since the timing of the binary search tree with 1,000 elements takes 5 seconds,
     which looks like $log_2(1,000)/2$ because that approximately results in 5 seconds,
     I would assume the timing of a binary search tree with 10,000 elements would take
     7 seconds because $log_2(10,000)/2$ would be approximately 7 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  1. As mentioned above, the hardware that was used to run the algorithm can be slow
     or the hardware used to run the algorithm has a lower memory capacity, which can result
     in the skewed results. Asymptotically, if more and more elements were tested using
     the same hardware then it would follow the same complexity, but like shown previosuly above,
     the expected results will be skewed, which would reason why the predicted asymptotic complexity
     was skewed. Smaller input sizes aren't impacted as greatly as larger inputs because
     smaller input sizes don't have as great of a memory strain since there are less elements to
     manipulate, which would explain why 1,000 elements were not impacted greatly, but 10,000 elements
     impacted the runtime laregly because of slow hardware or lower memory capacity.

  2. The difference in the time could be as simple as two different devices were used to run the algorithm.
     There is nothing that specifically states the same algorithm was run on the same device to
     get both timings. Different devices have different background tasks running at the same time
     as the the timing of the test, or different compilers were used if the code was the same. Different
     devices can also have different memory capacity, as mentioned above, or different CPU speeds, which
     can slow down the algorithm that is running. In practice, the same algorithm may not always be run
     on the same device, which can cause the difference in the predicted timing versus the actual timing
     because the device that ran the smaller input could have been run on superior hardware.
     (Help from the textbook)

  4. The asymptotic complexity given to the binary search tree algorithm for the worst
     case/average case is basically log(n), which we have established is from the drop of
     constants and that log bases don't matter asymptotically. Now since we have
     basically stated that log(n) is the worst case/average case, what if the element
     that was found in the tree with 1,000 elements was higher up in the tree, then the worst
     case/average case predicts. That would explain why the particular element was found faster
     because it was located closer to the root. Then, when the tree was expanded to 10,000 elements,
     the particular element we were looking for was pushed further down the tree. This would mean
     that our predicted calculations, were not the worst/average case, but rather geared towards the
     best/better cases, and the actual calcualtion of the worst case/ average case would need to change
     to accomodate to the drastic element location change. Since the same element is lower down
     in the tree and our calculations for worst case were established as wrong, then the new worst case
     calculations would lead closer to the resulted 100 seconds.


Add your answers to this markdown file.
