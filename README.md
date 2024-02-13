Problem 0


2. Prove the time complexity of the algorithms.

ANS:
By counting the number of functions that the recursive Fibonacci function calls, one can
examine its temporal complexity. It calls fib(n-1) and fib(n-2) for fib(n). Until the basic cases
of fib (0) and fib (1) are reached, each of these calls will make two more calls in turn.
The binary tree of calls, where each fib(n) call branches into two further calls, fib(n-1) and
fib(n-2), can be used to indicate the number of calls made. Since there are 2^h nodes at
height h in a binary tree, the number of calls made is proportional to 2^n, and the height of
this tree is n. As a result, O(2^n) is the temporal complexity of this crude recursive
Fibonacci implementation.


3. Comment on way's you could improve your implementation (you don't need to do it just
discuss it)

ANS:

The Fibonacci sequence can be applied in a number of ways to increase its
efficiency:

• Memory: This method includes caching the output of pricey function calls and
returning it when the same inputs are entered again. This would include saving the
result of fib(n) the first time it is computed and using it for subsequent calls with the
same n in the Fibonacci sequence.

• Bottom-Up Approach: The Fibonacci sequence can be calculated by iteration
rather than recursion by beginning with the base cases fib (0) and fib (1) and working
our way up to the required fib(n). Since each Fibonacci number is only calculated
once, this method only requires linear time, or O(n).

• Space Optimization in Iterative Approach: The next Fibonacci number in the
iterative bottom-up approach can be computed by simply keeping track of the
previous two. The space complexity can be decreased from O(n) to O (1) by simply
storing these two and updating them as we iterate, rather than storing all the
Fibonacci numbers up to n.

• Using Formulas: Binet's formula or matrix exponentiation can be used to directly
calculate the Fibonacci numbers, avoiding the requirement for numerous recursive
calls. Due to floating-point arithmetic difficulties, Binet's method may not be exact
for big n, but it can provide an approximation Fibonacci number in constant time, O
(1). On the other hand, matrix exponentiation is accurate and can calculate the nth
Fibonacci number in logarithmic time, O (log n).

• Tail Recursion: The recursive function could be rewritten to be tail-recursive in
languages that maximize tail recursion. In order to use constant stack space, the compiler
would be able to optimize the call stack as a result. Nevertheless, this would not be helpful
in Python without a manual call stack implementation because Python does not optimize
tail recursion.

• Using a Generator: A Python generator function can be used to generate numbers on the
spot without keeping the complete series in memory for applications that need Fibonacci
numbers in sequence
