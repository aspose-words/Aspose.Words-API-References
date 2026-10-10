---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية إزاحة مستويات القائمة عندما يتم تصدير المستند إلى تنسيق SaveFormat.TEXT في Java."
type: docs
weight: 692
url: /ar/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

يحدد كيفية إزاحة مستويات القائمة عندما يتم تصدير المستند إلى تنسيق [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Examples:** 

يوضح كيفية تكوين إزاحة القائمة عند حفظ المستند كنص عادي.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getCharacter()](#getCharacter) | يحصل على الحرف الذي سيُستخدم لإزاحة مستويات القائمة. |
| [getCount()](#getCount) | يحصل على عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة. |
| [setCharacter(char value)](#setCharacter-char) | يضبط الحرف الذي سيُستخدم لإزاحة مستويات القائمة. |
| [setCount(int value)](#setCount-int) | يضبط عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


يحصل على الحرف الذي سيُستخدم لإزاحة مستويات القائمة. القيمة الافتراضية هي '\\0'، وهذا يعني عدم وجود إزاحة.

 **Examples:** 

يوضح كيفية تكوين إزاحة القائمة عند حفظ المستند كنص عادي.

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
char - الحرف الذي سيُستخدم لإزاحة مستويات القائمة.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة. القيمة الافتراضية هي 0، وهذا يعني عدم وجود إزاحة.

 **Examples:** 

يوضح كيفية تكوين إزاحة القائمة عند حفظ المستند كنص عادي.

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
int - عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


يضبط الحرف الذي سيُستخدم لإزاحة مستويات القائمة. القيمة الافتراضية هي '\\0'، وهذا يعني عدم وجود إزاحة.

 **Examples:** 

يوضح كيفية تكوين إزاحة القائمة عند حفظ المستند كنص عادي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | char | الحرف الذي سيُستخدم لإزاحة مستويات القائمة. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


يضبط عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة. القيمة الافتراضية هي 0، وهذا يعني عدم وجود إزاحة.

 **Examples:** 

يوضح كيفية تكوين إزاحة القائمة عند حفظ المستند كنص عادي.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | عدد [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) التي تُستخدم كإزاحة لكل مستوى قائمة. |

