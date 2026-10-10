---
title: "TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words per Java"
description: "Specifica come i livelli di elenco sono indentati quando il documento viene esportato nel formato SaveFormat.TEXT in Java."
type: docs
weight: 692
url: /it/java/com.aspose.words/txtlistindentation/
---

**Inheritance:**
java.lang.Object
```
public class TxtListIndentation
```

Specifica come i livelli di elenco sono indentati quando il documento viene esportato nel formato [SaveFormat.TEXT](../../com.aspose.words/saveformat/\#TEXT).

Per saperne di più, visita l'articolo di documentazione [ Save a Document ][Save a Document].

 **Examples:** 

Mostra come configurare l'indentazione degli elenchi quando si salva un documento in testo semplice.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getCharacter()](#getCharacter) | Ottiene quale carattere utilizzare per indentare i livelli di elenco. |
| [getCount()](#getCount) | Ottiene quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco. |
| [setCharacter(char value)](#setCharacter-char) | Imposta quale carattere utilizzare per indentare i livelli di elenco. |
| [setCount(int value)](#setCount-int) | Imposta quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco. |
### getCharacter() {#getCharacter}
```
public char getCharacter()
```


Ottiene quale carattere utilizzare per indentare i livelli di elenco. Il valore predefinito è '\\0', il che significa che non c'è indentazione.

 **Examples:** 

Mostra come configurare l'indentazione degli elenchi quando si salva un documento in testo semplice.

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
char - Quale carattere utilizzare per indentare i livelli di elenco.
### getCount() {#getCount}
```
public int getCount()
```


Ottiene quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco. Il valore predefinito è 0, il che significa nessuna indentazione.

 **Examples:** 

Mostra come configurare l'indentazione degli elenchi quando si salva un documento in testo semplice.

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
int - Quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco.
### setCharacter(char value) {#setCharacter-char}
```
public void setCharacter(char value)
```


Imposta quale carattere utilizzare per indentare i livelli di elenco. Il valore predefinito è '\\0', il che significa che non c'è indentazione.

 **Examples:** 

Mostra come configurare l'indentazione degli elenchi quando si salva un documento in testo semplice.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | char | Quale carattere utilizzare per indentare i livelli di elenco. |

### setCount(int value) {#setCount-int}
```
public void setCount(int value)
```


Imposta quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco. Il valore predefinito è 0, il che significa nessuna indentazione.

 **Examples:** 

Mostra come configurare l'indentazione degli elenchi quando si salva un documento in testo semplice.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Quanti [getCharacter()](../../com.aspose.words/txtlistindentation/\#getCharacter) / [setCharacter(char)](../../com.aspose.words/txtlistindentation/\#setCharacter-char) utilizzare come indentazione per un livello di elenco. |

