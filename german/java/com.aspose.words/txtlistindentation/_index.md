---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument in das SaveFormat.TEXT-Format in Java exportiert wird."
type: docs
weight: 692
url: /de/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

Gibt an, wie Listenebenen eingerückt werden, wenn das Dokument in das [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT)-Format exportiert wird.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie das Einrücken von Listen beim Speichern eines Dokuments als Nur-Text konfiguriert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getCharacter()](#getCharacter) | Ermittelt, welches Zeichen für das Einrücken von Listenebenen verwendet wird. |
| [getCount()](#getCount) | Ermittelt, wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden. |
| [setCharacter(char value)](#setCharacter-char) | Legt fest, welches Zeichen für das Einrücken von Listenebenen verwendet wird. |
| [setCount(int value)](#setCount-int) | Legt fest, wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


Ermittelt, welches Zeichen für das Einrücken von Listenebenen verwendet wird. Der Standardwert ist '\\0', das bedeutet, dass keine Einrückung erfolgt.

 **Examples:** 

Zeigt, wie das Einrücken von Listen beim Speichern eines Dokuments als Nur-Text konfiguriert wird.

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
char – Welches Zeichen für das Einrücken von Listenebenen verwendet wird.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt, wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden. Der Standardwert ist 0, das bedeutet, dass keine Einrückung erfolgt.

 **Examples:** 

Zeigt, wie das Einrücken von Listen beim Speichern eines Dokuments als Nur-Text konfiguriert wird.

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
int – Wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


Legt fest, welches Zeichen für das Einrücken von Listenebenen verwendet wird. Der Standardwert ist '\\0', das bedeutet, dass keine Einrückung erfolgt.

 **Examples:** 

Zeigt, wie das Einrücken von Listen beim Speichern eines Dokuments als Nur-Text konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | char | Welches Zeichen für das Einrücken von Listenebenen verwendet wird. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


Legt fest, wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden. Der Standardwert ist 0, das bedeutet, dass keine Einrückung erfolgt.

 **Examples:** 

Zeigt, wie das Einrücken von Listen beim Speichern eines Dokuments als Nur-Text konfiguriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Wie viele [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) als Einrückung pro Listenebene verwendet werden. |

