we are given two strings, we want to merge them alternatively (basically one character at a time)

My solution:

```
public class Solution {

    public string MergeAlternately(string word1, string word2)

    {

        string merged = "";

        int i = 0;

  

        //While both strings havent been ran through

        while(i < word1.Length || i < word2.Length)

        {

            //If we still have length in the str1, add it to the merged

            if(i < word1.Length)

            {

                merged += word1[i];

            }

  

            //same here

            if(i < word2.Length)

            {

                merged += word2­[i];

            }

            i++;

        }

  

        //return the result

        return merged;

    }

}
```

