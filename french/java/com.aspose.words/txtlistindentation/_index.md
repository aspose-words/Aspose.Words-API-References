---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les niveaux de liste sont indentés lorsque le document est exporté au format SaveFormat.TEXT en Java."
type: docs
weight: 692
url: /fr/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

Spécifie comment les niveaux de liste sont indentés lorsque le document est exporté au format [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

Pour en savoir plus, consultez l'article de documentation [ Save a Document ][Save a Document].

 **Examples:** 

Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getCharacter()](#getCharacter) | Obtient le caractère à utiliser pour l'indentation des niveaux de liste. |
| [getCount()](#getCount) | Obtient combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste. |
| [setCharacter(char value)](#setCharacter-char) | Définit le caractère à utiliser pour l'indentation des niveaux de liste. |
| [setCount(int value)](#setCount-int) | Définit combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


Obtient le caractère à utiliser pour l'indentation des niveaux de liste. La valeur par défaut est '\\0', ce qui signifie qu'il n'y a pas d'indentation.

 **Examples:** 

Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.

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
char - Le caractère à utiliser pour l'indentation des niveaux de liste.
### getCount() {#getCount}
```
public int getCount()
```


Obtient combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste. La valeur par défaut est 0, ce qui signifie aucune indentation.

 **Examples:** 

Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.

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
int - Combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


Définit le caractère à utiliser pour l'indentation des niveaux de liste. La valeur par défaut est '\\0', ce qui signifie qu'il n'y a pas d'indentation.

 **Examples:** 

Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | char | Quel caractère utiliser pour l'indentation des niveaux de liste. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


Définit combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste. La valeur par défaut est 0, ce qui signifie aucune indentation.

 **Examples:** 

Montre comment configurer l'indentation des listes lors de l'enregistrement d'un document en texte brut.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Combien de [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utiliser comme indentation par niveau de liste. |

