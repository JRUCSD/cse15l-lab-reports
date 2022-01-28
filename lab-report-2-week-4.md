# CSE 15L Lab Report 2  Testing

## Change #1: File with an Image Reference  
[File](new-file.md)  
![First Error Image](error1.png)
![First Fix Image](fix1.png)
The result of this failure-inducing input, a markdown file containing only an image link, was the symptom of that image file being included in the output, when the expected output was an empty list, since the file contained no links `[]`. The bug was the program's inability to differentiate between links and images, fixed by skipping the algorithm to search for a link if an `!` was detected immediately before the first `[`. The bug was responsible for the symptom of an unexpected output, which itself was made apparent by the failure-inducing input not being properly handled by the program because of the bug.

## Change #2: File with no Valid Links  
[File](empty-file.md)  
![Second Error Image](error2.png)
![Second Fix Image](fix2.png)
This bug in particular encompassed a variety of symptoms, so our group focused on fixing one: invalid links which contained a space being included as valid links. In this case, the failure inducing input contained no valid links, but a bug in the program that could not detect an invalid link caused the symptom where invalid links appeared in the list when they should have been excluded.

## Change #3: File with [] but not ()  
[File](bracket-file.md)  
![Third Error Image](error3.png)
![Third Fix Image](fix3.png)  
In this instance, the bug arose from the program not being able to find a set of parentheses following a pair of brackets. 