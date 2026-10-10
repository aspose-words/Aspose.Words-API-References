---
title: "DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar opciones adicionales para el proceso de construcción de documentos en Java."
type: docs
weight: 164
url: /es/java/com.aspose.words/documentbuilderoptions/
---

**Inheritance:**
java.lang.Object
```
public class DocumentBuilderOptions
```

Permite especificar opciones adicionales para el proceso de construcción del documento.

 **Examples:** 

Muestra cómo ignorar el formato de tabla para el contenido posterior.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getContextTableFormatting()](#getContextTableFormatting) | True si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. |
| [getDesignMode()](#getDesignMode) | Corresponde al Modo de diseño en Microsoft Word. |
| [setContextTableFormatting(boolean value)](#setContextTableFormatting-boolean) | True si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. |
| [setDesignMode(boolean value)](#setDesignMode-boolean) | Corresponde al Modo de diseño en Microsoft Word. |
### getContextTableFormatting() {#getContextTableFormatting}
```
public boolean getContextTableFormatting()
```


True si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. El valor predeterminado es true.

 **Examples:** 

Muestra cómo ignorar el formato de tabla para el contenido posterior.

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
boolean - El valor  boolean  correspondiente.
### getDesignMode() {#getDesignMode}
```
public boolean getDesignMode()
```


Corresponde al Modo de diseño en Microsoft Word.

**Returns:**
boolean - El valor  boolean  correspondiente.
### setContextTableFormatting(boolean value) {#setContextTableFormatting-boolean}
```
public void setContextTableFormatting(boolean value)
```


True si el formato aplicado al contenido de la tabla no afecta al formato del contenido que le sigue. El valor predeterminado es true.

 **Examples:** 

Muestra cómo ignorar el formato de tabla para el contenido posterior.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setDesignMode(boolean value) {#setDesignMode-boolean}
```
public void setDesignMode(boolean value)
```


Corresponde al Modo de diseño en Microsoft Word.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

