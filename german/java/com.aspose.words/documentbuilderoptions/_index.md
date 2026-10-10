---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Angeben zusätzlicher Optionen für den Dokumenterstellungsprozess in Java."
type: docs
weight: 164
url: /de/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Ermöglicht das Angeben zusätzlicher Optionen für den Dokumenterstellungsprozess.

 **Examples:** 

Zeigt, wie die Tabellenformatierung für nachfolgenden Inhalt ignoriert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | True, wenn die auf Tabelleninhalt angewandte Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. |
| [getDesignMode()](#getDesignMode) | Entspricht dem Entwurfsmodus in Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | True, wenn die auf Tabelleninhalt angewandte Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Entspricht dem Entwurfsmodus in Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


True, wenn die auf Tabelleninhalt angewandte Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die Tabellenformatierung für nachfolgenden Inhalt ignoriert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Entspricht dem Entwurfsmodus in Microsoft Word.

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


True, wenn die auf Tabelleninhalt angewandte Formatierung die Formatierung des nachfolgenden Inhalts nicht beeinflusst. Der Standardwert ist true.

 **Examples:** 

Zeigt, wie die Tabellenformatierung für nachfolgenden Inhalt ignoriert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Entspricht dem Entwurfsmodus in Microsoft Word.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

