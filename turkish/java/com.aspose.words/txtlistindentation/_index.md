---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words Java için"
description: "Belirtilen belge, Java'da SaveFormat.TEXT formatına dışa aktarılırken liste seviyelerinin nasıl girintileneceğini belirtir."
type: docs
weight: 692
url: /tr/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

Belirtilen belge, [SaveFormat.TEXT](../../com.aspose.words/saveformat/\\#TEXT) formatına dışa aktarılırken liste seviyelerinin nasıl girintileneceğini belirtir.

Daha fazla bilgi edinmek için [ Save a Document ][Save a Document] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a list with three levels of indentation.
 builder.getListFormat().applyNumberDefault();
 builder.writeln("Item 1");
 builder.getListFormat().listIndent();
 builder.writeln("Item 2");
 builder.getListFormat().listIndent();
 builder.write("Item 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 // Set the "Character" property to assign a character to use
 // for padding that simulates list indentation in plaintext.
 txtSaveOptions.getListIndentation().setCharacter(' ');

 // Set the "Count" property to specify the number of times
 // to place the padding character for each list indent level.
 txtSaveOptions.getListIndentation().setCount(3);

 doc.save(getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

 String docText = getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt";

 TestUtil.fileContainsString("1. Item 1\r\n" +
         "   a. Item 2\r\n" +
         "      i. Item 3", docText);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCharacter()](#getCharacter) | Liste seviyelerini girintilemek için kullanılacak karakteri alır. |
| [getCount()](#getCount) | Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısını alır. |
| [setCharacter(char value)](#setCharacter-char) | Liste seviyelerini girintilemek için kullanılacak karakteri ayarlar. |
| [setCount(int value)](#setCount-int) | Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısını ayarlar. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


Liste seviyelerini girintilemek için kullanılacak karakteri alır. Varsayılan değer '\\0' dır, bu da girinti olmadığını gösterir.

 **Examples:** 

Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a list with three levels of indentation.
 builder.getListFormat().applyNumberDefault();
 builder.writeln("Item 1");
 builder.getListFormat().listIndent();
 builder.writeln("Item 2");
 builder.getListFormat().listIndent();
 builder.write("Item 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 // Set the "Character" property to assign a character to use
 // for padding that simulates list indentation in plaintext.
 txtSaveOptions.getListIndentation().setCharacter(' ');

 // Set the "Count" property to specify the number of times
 // to place the padding character for each list indent level.
 txtSaveOptions.getListIndentation().setCount(3);

 doc.save(getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

 String docText = getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt";

 TestUtil.fileContainsString("1. Item 1\r\n" +
         "   a. Item 2\r\n" +
         "      i. Item 3", docText);
 
```

**Returns:**
char - Liste seviyelerini girintilemek için kullanılacak karakter.
### getCount() {#getCount}
```
public int getCount()
```


Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısını alır. Varsayılan değer 0 dır, bu da girinti olmadığını gösterir.

 **Examples:** 

Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a list with three levels of indentation.
 builder.getListFormat().applyNumberDefault();
 builder.writeln("Item 1");
 builder.getListFormat().listIndent();
 builder.writeln("Item 2");
 builder.getListFormat().listIndent();
 builder.write("Item 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 // Set the "Character" property to assign a character to use
 // for padding that simulates list indentation in plaintext.
 txtSaveOptions.getListIndentation().setCharacter(' ');

 // Set the "Count" property to specify the number of times
 // to place the padding character for each list indent level.
 txtSaveOptions.getListIndentation().setCount(3);

 doc.save(getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

 String docText = getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt";

 TestUtil.fileContainsString("1. Item 1\r\n" +
         "   a. Item 2\r\n" +
         "      i. Item 3", docText);
 
```

**Returns:**
int - Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısı.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


Liste seviyelerini girintilemek için kullanılacak karakteri ayarlar. Varsayılan değer '\\0' dır, bu da girinti olmadığını gösterir.

 **Examples:** 

Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a list with three levels of indentation.
 builder.getListFormat().applyNumberDefault();
 builder.writeln("Item 1");
 builder.getListFormat().listIndent();
 builder.writeln("Item 2");
 builder.getListFormat().listIndent();
 builder.write("Item 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 // Set the "Character" property to assign a character to use
 // for padding that simulates list indentation in plaintext.
 txtSaveOptions.getListIndentation().setCharacter(' ');

 // Set the "Count" property to specify the number of times
 // to place the padding character for each list indent level.
 txtSaveOptions.getListIndentation().setCount(3);

 doc.save(getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

 String docText = getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt";

 TestUtil.fileContainsString("1. Item 1\r\n" +
         "   a. Item 2\r\n" +
         "      i. Item 3", docText);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | char | Liste seviyelerini girintilemek için kullanılacak karakter. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısını ayarlar. Varsayılan değer 0 dır, bu da girinti olmadığını gösterir.

 **Examples:** 

Bir belgeyi düz metin olarak kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a list with three levels of indentation.
 builder.getListFormat().applyNumberDefault();
 builder.writeln("Item 1");
 builder.getListFormat().listIndent();
 builder.writeln("Item 2");
 builder.getListFormat().listIndent();
 builder.write("Item 3");

 // Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how we save the document to plaintext.
 TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

 // Set the "Character" property to assign a character to use
 // for padding that simulates list indentation in plaintext.
 txtSaveOptions.getListIndentation().setCharacter(' ');

 // Set the "Count" property to specify the number of times
 // to place the padding character for each list indent level.
 txtSaveOptions.getListIndentation().setCount(3);

 doc.save(getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

 String docText = getArtifactsDir() + "TxtSaveOptions.TxtListIndentation.txt";

 TestUtil.fileContainsString("1. Item 1\r\n" +
         "   a. Item 2\r\n" +
         "      i. Item 3", docText);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bir liste seviyesi başına girinti olarak kullanılacak [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) sayısı. |

