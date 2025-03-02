Takes the bigger string of two and tries to find the greatest divider of it.

We tackle this by filtering out all the "bad" operations with the commutativity proprety of strings -> str1 + str2 = str2 + str1 means that there is a greatest common divisor....

Now that we have that filtered out we need to find the GDC...
To do so, we check which string is the longest and we use the modulo operator to get the remainder. 

```
public class Solution {

    //function to find greatest common divisor

    public int GCD(int n1, int n2){

        while (n1 != 0 && n2 != 0)

        {

            //Is the first string bigger than the second

            if (n1 > n2)

            {

                n1 %= n2;

            }

            else

            {

                n2 %= n1;

            }

        }

  

        return n1 | n2; //Returns the one that wont be 0 basically...

    }

  

    public string GcdOfStrings(string str1, string str2)

    {

        if(str1 + str2 != str2 + str1)

        {

            return "";

        }

  

        int gcdLen = GCD(str1.Length, str2.Length);

        return str1.Substring(0, gcdLen);

    }

}

```
