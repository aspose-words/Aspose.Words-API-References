---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se sangran los niveles de lista cuando el documento se exporta al formato SaveFormat.TEXT en Java."
type: docs
weight: 692
url: /es/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

Especifica cómo se sangran los niveles de lista cuando el documento se exporta al formato [SaveFormat.TEXT](../../com.aspose.words/saveformat/\\#TEXT).

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

 **Examples:** 

Muestra cómo configurar la sangría de listas al guardar un documento en texto sin formato.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getCharacter()](#getCharacter) | Obtiene qué carácter usar para sangrar los niveles de lista. |
| [getCount()](#getCount) | Obtiene cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista. |
| [setCharacter(char value)](#setCharacter-char) | Establece qué carácter usar para sangrar los niveles de lista. |
| [setCount(int value)](#setCount-int) | Establece cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


Obtiene qué carácter usar para sangrar los niveles de lista. El valor predeterminado es '\\0', lo que significa que no hay sangría.

 **Examples:** 

Muestra cómo configurar la sangría de listas al guardar un documento en texto sin formato.

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
char - Qué carácter usar para sangrar los niveles de lista.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa que no hay sangría.

 **Examples:** 

Muestra cómo configurar la sangría de listas al guardar un documento en texto sin formato.

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
int - Cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


Establece qué carácter usar para sangrar los niveles de lista. El valor predeterminado es '\\0', lo que significa que no hay sangría.

 **Examples:** 

Muestra cómo configurar la sangría de listas al guardar un documento en texto sin formato.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | char | Qué carácter usar para sangrar los niveles de lista. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


Establece cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista. El valor predeterminado es 0, lo que significa que no hay sangría.

 **Examples:** 

Muestra cómo configurar la sangría de listas al guardar un documento en texto sin formato.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Cuántos [getCharacter()](../../com.aspose.words/txtlistindentation/\\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\\#setCharacter-char) usar como sangría por cada nivel de lista. |

