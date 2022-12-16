### Task №1(7kyu)

Your task is to split the chocolate bar of given dimension n x m into small squares. Each square is of size 1x1 and
unbreakable. Implement a function that will return minimum number of breaks needed.

For example if you are given a chocolate bar of size 2 x 1 you can split it to single squares in just one break, but for
size 3 x 1 you must do two breaks.

If input data is invalid you should return 0 (as in no breaks are needed if we do not have any chocolate to split).
Input will always be a non-negative integer.

[Task_link](https://www.codewars.com/kata/534ea96ebb17181947000ada)

#### Solution

~~~ Java
public class Chocolate{
    public static int breakChocolate(int n, int m) {
        if(((n * m) - 1) < 0) {
            return 0;
        } else {
            return (n * m) - 1;
        }
    }
}
~~~

#### Fav Solution

~~~ Java

~~~

### Task №2(7kyu)

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines
whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

Example: (Input --> Output)

"Dermatoglyphics" --> true "aba" --> false "moOse" --> false (ignore letter case)

~~~ Java
isIsogram "Dermatoglyphics" = true
isIsogram "moose" = false
isIsogram "aba" = false
~~~

[Task_link](https://www.codewars.com/kata/54ba84be607a92aa900000f1)

#### Solution

~~~ Java
public class isogram {
    public static boolean isIsogram(String str) {
      str = str.toLowerCase();
      char  str_1[] = str.toCharArray();
      for (int  i = 0; i < str.length(); i++) {
         for (int j = i + 1; j < str.length(); j++) {
             if (str_1[i] == str_1[j]) {
                 return false;
             }
          }
       }
      return true;
 }  
}   
~~~

#### Fav Solution

~~~ Java
class isogram {
    public static boolean isIsogram(String str) {
        return str.toLowerCase()
                  .chars()
                  .distinct()
                  .count() == str.length();
    }
}
~~~

