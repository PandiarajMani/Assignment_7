
*********************Assignment 7**************************
Task 1
******
Given a list of strings - List[String] (“alpha”, “gamma”, “omega”, “zeta”, “beta”)
- Find count of all strings with length 4.
- Convert the list of string to a list of integers, where each string is mapped to its
corresponding length.
- Find count of all strings which contain alphabet ‘m’.
- Find the count of all strings which start with the alphabet ‘a’.

**************************************************************
//*Given a list of strings - List[String] (“alpha”, “gamma”, “omega”, “zeta”, “beta”)
- Find count of all strings with length 4

scala> val ArrayList = List[String]("alpha","gamma","omega","zeta","beta")
ArrayList: List[String] = List(alpha, gamma, omega, zeta, beta)



scala> val count = ArrayList.count(s => s.length==4)

count: Int = 2
***************************************************************
//*Convert the list of string to a list of integers, where each string is mapped to its
corresponding length

scala> val modified_list = ArrayList.map(s => s.length)
modified_list: List[Int] = List(5, 5, 5, 4, 4)

scala> 
***************************************************************

//* Find count of all strings which contain alphabet ‘m’.

scala> val find_m = ArrayList.count(s => s.contains('m'))
find_m: Int = 2
***************************************************************

//*Find the count of all strings which start with the alphabet ‘a’.

scala> val starting_with_a = ArrayList.filter(s => s(0)=='a').length
starting_with_a: Int = 1

scala> 


###########################################################################

Task 2
******
Create a list of tuples, where the 1st element of the tuple is an int and the second
element is a string.
Example - ((1, ‘alpha’), (2, ‘beta’), (3, ‘gamma’), (4, ‘zeta’), (5, ‘omega’))
- For the above list, print the numbers where the corresponding string length is 4.
- find the average of all numbers, where the corresponding string contains alphabet ‘m’
or alphabet ‘z’.

//*- For the above list, print the numbers where the corresponding string length is 4


scala> val ArrayList1 = List[(Int,String)]((1,"alpha"),(2,"beta"),(3,"gamma"),(4,"zeta"),(5,"omega"))
ArrayList1: List[(Int, String)] = List((1,alpha), (2,beta), (3,gamma), (4,zeta), (5,omega))

scala>

scala> val number_length4 = ArrayList1.filter(s => s._2.length==4).map(x => x._1)
number_length4: List[Int] = List(2, 4)

scala> 
******************************************************************************

//*find the average of all numbers, where the corresponding string contains alphabet ‘m’
or alphabet ‘z’

scala> val average_num = ArrayList1.filter(s => s._2.contains('m')|| s._2.contains('z')).map(x => x.swap)
average_num: List[(String, Int)] = List((gamma,3), (zeta,4), (omega,5))

scala> 

scala> val average_num_sum = average_num.size
average_num_sum: Int = 3

scala> 

scala> val final_sum = average_num.map(x => x._2).sum
final_sum: Int = 12

scala>

scala> val final_average = final_sum/average_num_sum
final_average: Int = 4

scala>  

***********************************************************************************
