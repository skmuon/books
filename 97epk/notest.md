#97 Things Every Prorgammer Should Know

Reading notes from the **97 Things Every Programmer Should know** 

## Act with Prudence
1. Pressure is inevitable irrespective of the schedule (Relaxed or Tight)
2. Choose "Do it right" instead of "Do it quick"
3. Avoid **Technical Debt**
4. Short cut in the code make scalable and refactoring hard
5. Don't wait, fix issues early
6. Fix the root cause, not the symptom
7. If technical debot is taken, pay it back quickly 
8. Pay off technical debit as soon as possible. It would be imprudent to do otherwise

## Apply Functional Programming Principles
1. Master Functional Programming paradigm (Improves code quality)
2. Functional paradigm exhibits higher degree of referential transparency
3. Referential transparency - Imples functions consistently yield same results for the same input, irrespective of where and when they are invoked
4. Leading cause of defects in imperative code is attributable to mutable variables
5. Visibility semantics can help to mitigate mutable variables


## Ask, "What Would the User Do?"(You Are Not the User)
1. People don't think like programmers (False consensus bias)
2. Watch users in action, ask them to use the software
3. Don't give specific instructions to users, when they are testing
4. When debugging, follow the same steps as done by the user

## Automate Your Coding Standard
1. Automate the coding standard, i.e. checks to adherence
2. Follow the Automation process
  * Code formatting should be part of build process and run automatically for everyone
  * Use static code analysis tools to scan the code for unwanted antipatterns, break the build on violation
  * Learn to configure those tools so that you can scan for your own, project specific antipatterns
  * Do not only measure test coverage, but automatically check the results, too.
3. Keep the coding standard dynamic and not static

## Beauity In Simplicity
1. Beauty of style and harmony and grace and good rhythm depends on simplicity
2. Code should have
  * Readability
  * Maintainability
  * Speed of development
  * Elusive quality of beauty
3. Study other people's code
4. Beautiful code is simple code, each induvidual part is kept simple with simple responsibilites and simple relationships with other parts of the system
5. Systems should be easy to maintain, clean and testable
6. Beauty is born of and found in simplicity

## Before You Refactor
1. First write tests against existing code based. Will help to get insights into strength and weakness
2. Refactored code should be better than the original one
3. Avoid the temptation to rewrite everything. Reuse the code
4. Don't throw away production code, it has taken efforts to make it
5. Many incremental changes are better than the one massive change
6. Test after each iteration of refactoring
7. Personal preferences and ego should't get in the way
8. New technology is an insuffiecent reason to refactor
9. Remember that humans make mistakes

## Beware the share
1. Beware of what code, libaries you share from open sources
2. Reuse stuff based on current context

## The Boy Socut Rule
1. "Always leave the campground cleaner than you found it"
2. "Try and leave this world a little better than you found it" 


## Check Your Code First Before Looking to Blame Others
1. Question your assumptions and the assumptions of others
2. Verify the steps leading to the problem
3. If the bug cannot be pinned down and if you start thinking about the compiler, then check stack corruption
4. "Once you eliminate the improbable, whatever remains, no matter how impossible must be the truth"


## Choose Your Tools with Care
1. Choose the right mix of tools

## Code in the Language of the Domain
1. Code using domain terms
2. Make domain concepts explict in your code, helps other programmers

## Code Is Design

## Code Layout Matters
1. Easy to scan the code
2. Expressive layout
3. Compatc format, yeilds high information density on the screen

## Coding with Reason
1. Do code reveiw to improve code quality and reduce defect rate


