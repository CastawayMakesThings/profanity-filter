# Profanity Filter
Simple and fast dictionary-based multi-language profanity filter written in Java.

### Quick Usage
There are two simple methods used you should know for basic use of this tool. But first, create the ProfanityFilter object:

```java
  ProfanityFilter filter = new ProfanityFilter;
```
That is all the initialization you have to do. To check if a string contains bad language, simply use the test method. It takes in the language and the string, and outputs true if it contains bad language, and false if it is clean.

```java
  String cleanString = "Hello there!";
  String dirtyString = "What the f**k?" //I have censored this for the docs, but pretend it is actually there.";

  ProfanityFilter filter = new ProfanityFilter();
  
  System.out.println(filter.test("en", cleanString)); //Would print 'false'
  System.out.println(filter.test("en", dirtyString)); //Would print 'true'
```
The other method is for actually finding swear words. That is the find method. It also takes in a language and string, and returns both the bad word found and it's score between 0 and 1. If no swear words are found, it simply returns nothing. Note, it can only find one at a time. 

```java
  
  ProfanityFilter pf = new ProfanityFilter();
  System.out.println(pf.find("en", "What the f**k is up?")); //Once again, the word is censored.
  //This would return "f**k	0.6570979"
```


### All languages

| Code | Language       | Code | Language       |
|------|----------------|------|----------------|
| ar   | Arabic         | az   | Azerbaijani    |
| bg   | Bulgarian      | bs   | Bosnian        |
| ca   | Catalan        | cs   | Czech          |
| da   | Danish         | de   | German         |
| el   | Greek          | en   | English        |
| es   | Spanish        | et   | Estonian       |
| fi   | Finnish        | fr   | French         |
| ga   | Irish          | he   | Hebrew         |
| hi   | Hindi          | hr   | Croatian       |
| hu   | Hungarian      | hy   | Armenian       |
| id   | Indonesian     | is   | Icelandic      |
| it   | Italian        | ja   | Japanese       |
| ka   | Georgian       | ko   | Korean         |
| lt   | Lithuanian     | lv   | Latvian        |
| mk   | Macedonian     | ms   | Malay          |
| mt   | Maltese        | no   | Norwegian      |
| nl   | Dutch          | pl   | Polish         |
| pt   | Portuguese     | ro   | Romanian       |
| ru   | Russian        | sk   | Slovak         |
| sl   | Slovenian      | sq   | Albanian       |
| sr   | Serbian        | sv   | Swedish        |
| sw   | Swahili        | th   | Thai           |
| tl   | Tagalog        | tr   | Turkish        |
| uk   | Ukrainian      | vi   | Vietnamese     |
| xh   | Xhosa          | zh   | Chinese        |
| zu   | Zulu           |      |                |

#### Under Apache 2.0 License.
