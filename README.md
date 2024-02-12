[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  1. The asymptotic analysis may be leading because of the constants that were
     were dropped when solving for the complexity. They actually affect the runtime
     of the algorithm (specific timing), where as the complexity simply explains
     how runtime should look.

  2. The arrangement of the input can also make the asymptotic analysis differ.
     The average case complexity covers a wide range of possibilities, so the
     specific input given can act differently during runtime because average case
     covers what the average case is deemed.

  3. Outside factors, like what is simultaneously running, can also make the
     asymptotic analysis be misleading because having multiple process
     running at the same time can increase the runtime of the algorithm. 

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  1. Since the asymptotic complexity of a binary search tree is $\Theta(log_2(n))$,
     I would assume it takes around 14 seconds approximately because $log_2(10000)$
     is approximately 14 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  1. The outside factors that were running alongside the timing of the runtime
     could have stretched how long it took to find the particular element in
     a binary search tree.

  2. There was an unbalanced tree/unbalanced input, so the algorithm could not
     accuratetly locate the element in the approximated time.

  3. The constants that were dropped when solving for the complexity would
     have changed the scaling of the runtime, which means the actual runtime
     should have been greater, but it was scaled down to show asymptotic complexity.


Add your answers to this markdown file.
