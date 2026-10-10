---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier des options supplémentaires pour le processus de génération de documents en Java."
type: docs
weight: 164
url: /fr/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Permet de spécifier des options supplémentaires pour le processus de création du document.

 **Examples:** 

Montre comment ignorer le formatage du tableau pour le contenu suivant.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. |
| [getDesignMode()](#getDesignMode) | Correspond au mode Conception dans Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Correspond au mode Conception dans Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. La valeur par défaut est  true .

 **Examples:** 

Montre comment ignorer le formatage du tableau pour le contenu suivant.

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
boolean - La valeur  boolean  correspondante.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Correspond au mode Conception dans Microsoft Word.

**Returns:**
boolean - La valeur  boolean  correspondante.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


Vrai si le formatage appliqué au contenu du tableau n'affecte pas le formatage du contenu qui le suit. La valeur par défaut est  true .

 **Examples:** 

Montre comment ignorer le formatage du tableau pour le contenu suivant.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Correspond au mode Conception dans Microsoft Word.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

