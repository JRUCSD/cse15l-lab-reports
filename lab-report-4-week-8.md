# CSE 15L Lab Report 4: More MarkdownParse Testing

### Expected Output of Markdown Snippets:
![snippet1](snippet1Expected.png) ![snippet2](snippet2Expected.png) ![snippet3](snippet3Expected.png)

### Testing the Snippets

```
@Test
public void getLinksTestSnippet1() throws IOException{
    Path fileName = Path.of("snippet1.md");
    String contents = Files.readString(fileName);
    assertEquals(List.of("`google.com", "google.com", "ucsd.edu"), MarkdownParse.getLinks(contents));
}
@Test
public void getLinksTestSnippet2() throws IOException{
    Path fileName = Path.of("snippet2.md");
    String contents = Files.readString(fileName);
    assertEquals(List.of("a.com(())", "a.com(())", "example.com"), MarkdownParse.getLinks(contents));
}
@Test
public void getLinksTestSnippet3() throws IOException{
    Path fileName = Path.of("snippet3.md");
    String contents = Files.readString(fileName);
    assertEquals(List.of("https://www.twitter.com", "https://ucsd-cse15l-w22.github.io/", "https://cse.ucsd.edu/"), MarkdownParse.getLinks(contents);
}
```

[My MarkdownParse](https://github.com/JRUCSD/markdown-parse)  
### All Tests Failed
![failed tests](myFailure.png)  
[Reviewed MarkdownParse](https://github.com/w2llS/markdown-parse)  
### All Tests Failed
![failed tests](reviewFailure.png)  

[<- Back](index.md)