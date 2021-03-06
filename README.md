# Blue-Gene-Jr.

Blue Gene, Jr.

Description
Inspired by IBM's Blue Gene project, the CEO of Universal Biological Machinery (UBM), has called on you, UBM's top software engineer, to develop a program that will calculate the mutation of the Areopagus-virus, a virus discovered on Mars by your company's privately-subsidized (top-secret) space program.

Input

Input to this problem will consist of a (non-empty) series of up to 100 data sets. Each data set will be formatted according to the following description, and there will be no blank lines separating data sets.
A single data set has 3 components:


    Start line - A single line, "START N", where 1 <= N <= 20.
    Viral code - A sequence of N alphanumeric characters. Alphanumeric characters will consist of an uppercase letter (A-Z) or a digit (0-9).
    End line - A single line, "END"


Following the final data set will be a single line, "ENDOFINPUT".

Output

For each data set, there will be exactly one output set, and there will be no blank lines separating output sets.

A single output set consists of a single line of the viral code after it has stabilized (through mutating).

The viral code will mutate according to the following rules:


    Initially the first viral segment to mutate begins with the first alphanumeric character of the viral code and ends with the rightmost alphanumeric character of the code.
    If the first alphanumeric character of a viral segment is a letter (A-Z), that alphanumeric character is considered "unstable", and will mutate into n, where n is the number of mutations that occur to the viral segment immediately to the unstable alphanumeric character's right (see #5), unless n is greater than 9, in which case the unstable alphanumeric character will mutate into n % 10. Also, if there is no viral segment immediately to the right of the unstable alphanumeric character, the unstable alphanumeric character will mutate into 0.
    If the first alphanumeric character of a viral segment, n, is a positive number (1-9), that alphanumeric character is also considered "unstable", and will mutate into n-1. It also causes the viral segment beginning with the alphanumeric character n alphanumeric characters to its right and ending with the rightmost alphanumeric character of the viral code to mutate. If there is no alphanumeric character n alphanumeric characters to its right, then the viral segment immediately to its right (see #5), if one exists, will mutate.
    If the first alphanumeric character of a viral segment is 0, that alphanumeric character is considered "stable", and will not mutate (the alphanumeric character will remain a 0 and a mutation will not be considered to have occurred).
    A viral segment immediately to the right of an alphanumeric character begins with the alphanumeric character one position to its right and ending with the rightmost alphanumeric character of the viral code.

Sample Input

START 1

A
END
START 4
A1B2
END
START 15
A3B2CCC4AD1232R
END
START 15
0ABCDEFGHIJKLMN
END
START 11
ABCDEFGHIJK
END
START 10
9AAAAAAAAA
END
ENDOFINPUT

Sample Output

0
3011
82B26543AD11310
0ABCDEFGHIJKLMN
09876543210
8AAAAAAAA0
