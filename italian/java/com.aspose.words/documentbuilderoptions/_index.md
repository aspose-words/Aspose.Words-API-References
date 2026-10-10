---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare opzioni aggiuntive per il processo di creazione del documento in Java."
type: docs
weight: 164
url: /it/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Consente di specificare opzioni aggiuntive per il processo di costruzione del documento.

 **Examples:** 

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. |
| [getDesignMode()](#getDesignMode) | Corrisponde alla Modalità Progettazione in Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Corrisponde alla Modalità Progettazione in Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. Il valore predefinito è  true .

 **Examples:** 

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Corrisponde alla Modalità Progettazione in Microsoft Word.

**Returns:**
boolean - Il valore booleano corrispondente.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. Il valore predefinito è  true .

 **Examples:** 

Mostra come ignorare la formattazione della tabella per il contenuto successivo.

```

 Document doc = new Document();
 DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
 builderOptions.setContextTableFormatting(true);
 DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

 // Adds content before the table.
 // Default font size is 12.
 builder.writeln("Font size 12 here.");
 builder.startTable();
 builder.insertCell();
 // Changes the font size inside the table.
 builder.getFont().setSize(5.0);
 builder.write("Font size 5 here");
 builder.insertCell();
 builder.write("Font size 5 here");
 builder.endRow();
 builder.endTable();

 // If ContextTableFormatting is true, then table formatting isn't applied to the content after.
 // If ContextTableFormatting is false, then table formatting is applied to the content after.
 builder.writeln("Font size 12 here.");

 doc.save(getArtifactsDir() + "Table.ContextTableFormatting.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Corrisponde alla Modalità Progettazione in Microsoft Word.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

