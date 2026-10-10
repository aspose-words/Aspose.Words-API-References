---
title: "ImportFormatOptions"
linktitle: "ImportFormatOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar varias opciones de importación para formatear la salida en Java."
type: docs
weight: 401
url: /es/java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Permite especificar varias opciones de importación para formatear la salida.

Para obtener más información, visite el artículo de documentación [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Muestra cómo resolver estilos duplicados al insertar documentos.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | Obtiene un valor booleano que especifica si se debe ajustar el espaciado de oraciones y palabras automáticamente. |
| [getAppendDocumentWithNewPage()](#getAppendDocumentWithNewPage) | Obtiene un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [getForceCopyStyles()](#getForceCopyStyles) | Obtiene un valor booleano que indica si copiar estilos en conflicto en el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | Obtiene un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | Obtiene un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Obtiene un valor booleano que especifica cómo se importará la numeración cuando haya conflictos entre los documentos de origen y destino. |
| [getMergePastedLists()](#getMergePastedLists) | Obtiene un valor booleano que especifica si las listas pegadas se combinarán con las listas circundantes. |
| [getResolveThemeColors()](#getResolveThemeColors) | Obtiene un valor booleano que especifica si se deben resolver forzadamente los colores de tema de las formas. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Obtiene un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | Establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. |
| [setAppendDocumentWithNewPage(boolean value)](#setAppendDocumentWithNewPage-boolean) | Establece un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\\_PAGE](../../com.aspose.words/sectionstart/\\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | Establece un valor booleano que indica si se deben copiar los estilos conflictivos en el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | Establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignore si se utiliza el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING). |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | Establece un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignore si se utiliza el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING). |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Establece un valor booleano que especifica cómo se importará la numeración cuando haya conflictos en los documentos de origen y destino. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Establece un valor booleano que especifica si las listas pegadas se combinarán con las listas circundantes. |
| [setResolveThemeColors(boolean value)](#setResolveThemeColors-boolean) | Establece un valor booleano que especifica si se deben resolver forzadamente los colores de tema de las formas. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


Obtiene un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. El valor predeterminado es false.

 **Examples:** 

Muestra cómo ajustar automáticamente el espaciado de oraciones y palabras.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Returns:**
boolean - Un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras.
### getAppendDocumentWithNewPage() {#getAppendDocumentWithNewPage}
```
public boolean getAppendDocumentWithNewPage()
```


Obtiene un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

El valor predeterminado es  true .

 **Remarks:** 

Tenga en cuenta que esta opción solo es relevante para el método **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** y no tiene efecto en otros métodos relacionados con la importación.

 **Examples:** 

Muestra cómo preservar el tipo de sección original.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Returns:**
boolean - Un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\\_PAGE](../../com.aspose.words/sectionstart/\\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Obtiene un valor booleano que indica si se deben copiar los estilos conflictivos en el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING). El valor predeterminado es false.

 **Remarks:** 

Por defecto, si ya existe un estilo coincidente en un documento de destino, el formato del estilo de origen se expande en atributos directos del nodo y el estilo de este nodo se restablece al valor predeterminado.

Cuando esta opción se establece en true, el estilo de origen se copiará forzadamente al documento de destino con un nombre único y se aplicará al nodo importado.

Nota: en este caso no se garantiza que el formato del nodo importado en el documento de destino se preserve.

 **Examples:** 

Muestra cómo copiar forzadamente los estilos de origen con nombres únicos.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Returns:**
boolean - Un valor booleano que indica si se deben copiar los estilos conflictivos en el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING).
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Obtiene un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignore si se utiliza el modo [ImportFormatMode.KEEP\\_SOURCE\\_FORMATTING](../../com.aspose.words/importformatmode/\\#KEEP-SOURCE-FORMATTING). El valor predeterminado es true.

 **Examples:** 

Muestra cómo especificar si se ignora o no el formato de origen del contenido de encabezados/pies de página.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Returns:**
boolean - Un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Obtiene un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). El valor predeterminado es true.

 **Examples:** 

Muestra cómo gestionar el formato de los cuadros de texto al anexar un documento.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Returns:**
boolean - Un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Obtiene un valor booleano que especifica cómo se importará la numeración cuando haya conflictos en los documentos de origen y destino. El valor predeterminado es false.

 **Examples:** 

Muestra cómo importar un documento con listas numeradas.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

Muestra cómo resolver un conflicto al importar documentos que tienen listas con el mismo identificador de definición de lista.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

Muestra cómo resolver conflictos de numeración de listas en los documentos de origen y destino.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Returns:**
boolean - Un valor booleano que especifica cómo se importará la numeración cuando haya conflictos en los documentos de origen y destino.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Obtiene un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es false.

 **Examples:** 

Muestra cómo fusionar listas de un documento.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
boolean - Un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes.
### getResolveThemeColors() {#getResolveThemeColors}
```
public boolean getResolveThemeColors()
```


Obtiene un valor booleano que especifica si se deben resolver forzosamente los colores de tema de las formas. El valor predeterminado es false.

 **Remarks:** 

Tenga en cuenta que esta opción solo es relevante para el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Normalmente, Aspose.Words no resuelve los colores de tema de origen al importar estilos que pueden preservarse sin expandir los atributos de formato en atributos directos. Sin embargo, en este caso los colores reales de las formas importadas pueden diferir de los que tenían en el documento original. La razón es que los colores de tema difieren entre los documentos de origen y destino. Establecer esta opción en true obliga a resolver los colores de tema de las formas de origen y, por lo tanto, a preservar el color real de las formas que tienen en el documento de origen.

 **Examples:** 

Muestra cómo importar un nodo resolviendo los colores de tema de origen de las formas.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Returns:**
boolean - Un valor booleano que especifica si se deben resolver forzosamente los colores de tema de las formas.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Obtiene un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es false.

 **Remarks:** 

Cuando esta opción está **enabled**, el estilo de origen se expandirá en atributos directos dentro del documento de destino, si se usa el modo de importación [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Cuando esta opción está **disabled**, el estilo de origen se expandirá solo si está numerado. Los atributos existentes del destino no se sobrescribirán, incluidas las listas.

 **Examples:** 

Muestra cómo resolver estilos duplicados al insertar documentos.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Returns:**
boolean - Un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


Establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. El valor predeterminado es false.

 **Examples:** 

Muestra cómo ajustar automáticamente el espaciado de oraciones y palabras.

```

 Document srcDoc = new Document();
 Document dstDoc = new Document();

 DocumentBuilder builder = new DocumentBuilder(srcDoc);
 builder.write("Dolor sit amet.");

 builder = new DocumentBuilder(dstDoc);
 builder.write("Lorem ipsum.");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setAdjustSentenceAndWordSpacing(true); }
 builder.insertDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 Assert.assertEquals("Lorem ipsum. Dolor sit amet.", dstDoc.getFirstSection().getBody().getFirstParagraph().getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Valor booleano que especifica si se debe ajustar automáticamente el espaciado de oraciones y palabras. |

### setAppendDocumentWithNewPage(boolean value) {#setAppendDocumentWithNewPage-boolean}
```
public void setAppendDocumentWithNewPage(boolean value)
```


Establece un valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\\_PAGE](../../com.aspose.words/sectionstart/\\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**.

El valor predeterminado es  true .

 **Remarks:** 

Tenga en cuenta que esta opción solo es relevante para el método **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)** y no tiene efecto en otros métodos relacionados con la importación.

 **Examples:** 

Muestra cómo preservar el tipo de sección original.

```

 Document dstDoc = new Document();
 Document srcDoc = new Document();

 srcDoc.getFirstSection().getPageSetup().setSectionStart(SectionStart.CONTINUOUS);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setAppendDocumentWithNewPage(false);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 Assert.assertEquals(SectionStart.CONTINUOUS, dstDoc.getSections().get(1).getPageSetup().getSectionStart());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Valor booleano que indica si se debe cambiar el tipo de la primera sección importada a [SectionStart.NEW\_PAGE](../../com.aspose.words/sectionstart/\#NEW-PAGE) de forma forzada al llamar a **M:Aspose.Words.Document.AppendDocument(Aspose.Words.Document,Aspose.Words.ImportFormatMode,Aspose.Words.ImportFormatOptions)**. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Establece un valor booleano que indica si copiar estilos en conflicto en modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). El valor predeterminado es false.

 **Remarks:** 

Por defecto, si ya existe un estilo coincidente en un documento de destino, el formato del estilo de origen se expande en atributos directos del nodo y el estilo de este nodo se restablece al valor predeterminado.

Cuando esta opción se establece en true, el estilo de origen se copiará forzadamente al documento de destino con un nombre único y se aplicará al nodo importado.

Nota: en este caso no se garantiza que el formato del nodo importado en el documento de destino se preserve.

 **Examples:** 

Muestra cómo copiar forzadamente los estilos de origen con nombres únicos.

```

 // Both documents contain MyStyle1 and MyStyle2, MyStyle3 exists only in a source document.
 Document srcDoc = new Document(getMyDir() + "Styles source.docx");
 Document dstDoc = new Document(getMyDir() + "Styles destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setForceCopyStyles(true); }
 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 ParagraphCollection paras = dstDoc.getSections().get(1).getBody().getParagraphs();

 Assert.assertEquals(paras.get(0).getParagraphFormat().getStyle().getName(), "MyStyle1_0");
 Assert.assertEquals(paras.get(1).getParagraphFormat().getStyle().getName(), "MyStyle2_0");
 Assert.assertEquals(paras.get(2).getParagraphFormat().getStyle().getName(), "MyStyle3");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Un valor booleano que indica si copiar estilos en conflicto en modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). El valor predeterminado es true.

 **Examples:** 

Muestra cómo especificar si se ignora o no el formato de origen del contenido de encabezados/pies de página.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 // If 'IgnoreHeaderFooter' is false then the original formatting for header/footer content
 // from "Header and footer types.docx" will be used.
 // If 'IgnoreHeaderFooter' is true then the formatting for header/footer content
 // from "Document.docx" will be used.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Establece un valor booleano que especifica que el formato de origen del contenido de cuadros de texto se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). El valor predeterminado es true.

 **Examples:** 

Muestra cómo gestionar el formato de los cuadros de texto al anexar un documento.

```

 // Create a document that will have nodes from another document inserted into it.
 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 builder.writeln("Hello world!");

 // Create another document with a text box, which we will import into the first document.
 Document srcDoc = new Document();
 builder = new DocumentBuilder(srcDoc);

 Shape textBox = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 100.0);
 builder.moveTo(textBox.getFirstParagraph());
 builder.getParagraphFormat().getStyle().getFont().setName("Courier New");
 builder.getParagraphFormat().getStyle().getFont().setSize(24.0);
 builder.write("Textbox contents");

 // Set a flag to specify whether to clear or preserve text box formatting
 // while importing them to other documents.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreTextBoxes(ignoreTextBoxes);

 // Import the text box from the source document into the destination document,
 // and then verify whether we have preserved the styling of its text contents.
 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);
 Shape importedTextBox = (Shape) importer.importNode(textBox, true);
 dstDoc.getFirstSection().getBody().getParagraphs().get(1).appendChild(importedTextBox);

 if (ignoreTextBoxes) {
     Assert.assertEquals(12.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Times New Roman", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 } else {
     Assert.assertEquals(24.0d, importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getSize());
     Assert.assertEquals("Courier New", importedTextBox.getFirstParagraph().getRuns().get(0).getFont().getName());
 }

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.IgnoreTextBoxes.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | boolean | Un valor booleano que especifica que el formato de origen del contenido de cuadros de texto se ignora si se usa el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING). |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Establece un valor booleano que especifica cómo se importará la numeración cuando haya conflictos entre los documentos de origen y destino. El valor predeterminado es false.

 **Examples:** 

Muestra cómo importar un documento con listas numeradas.

```

 Document srcDoc = new Document(getMyDir() + "List source.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 Assert.assertEquals(dstDoc.getLists().getCount(), 4);

 ImportFormatOptions options = new ImportFormatOptions();

 // If there is a clash of list styles, apply the list format of the source document.
 // Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
 // Set the "KeepSourceNumbering" property to "true" import all clashing
 // list style numbering with the same appearance that it had in the source document.
 options.setKeepSourceNumbering(isKeepSourceNumbering);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);
 dstDoc.updateListLabels();

 if (isKeepSourceNumbering)
     Assert.assertEquals(dstDoc.getLists().getCount(), 5);
 else
     Assert.assertEquals(dstDoc.getLists().getCount(), 4);
 
```

Muestra cómo resolver un conflicto al importar documentos que tienen listas con el mismo identificador de definición de lista.

```

 Document srcDoc = new Document(getMyDir() + "List with the same definition identifier - source.docx");
 Document dstDoc = new Document(getMyDir() + "List with the same definition identifier - destination.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();

 // Set the "KeepSourceNumbering" property to "true" to apply a different list definition ID
 // to identical styles as Aspose.Words imports them into destination documents.
 importFormatOptions.setKeepSourceNumbering(true);
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, importFormatOptions);

 dstDoc.updateListLabels();
 
```

Muestra cómo resolver conflictos de numeración de listas en los documentos de origen y destino.

```

 // Open a document with a custom list numbering scheme, and then clone it.
 // Since both have the same numbering format, the formats will clash if we import one document into the other.
 Document srcDoc = new Document(getMyDir() + "Custom list numbering.docx");
 Document dstDoc = srcDoc.deepClone();

 // When we import the document's clone into the original and then append it,
 // then the two lists with the same list format will join.
 // If we set the "KeepSourceNumbering" flag to "false", then the list from the document clone
 // that we append to the original will carry on the numbering of the list we append it to.
 // This will effectively merge the two lists into one.
 // If we set the "KeepSourceNumbering" flag to "true", then the document clone
 // list will preserve its original numbering, making the two lists appear as separate lists.
 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setKeepSourceNumbering(keepSourceNumbering);

 NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KEEP_DIFFERENT_STYLES, importFormatOptions);
 for (Paragraph paragraph : srcDoc.getFirstSection().getBody().getParagraphs()) {
     Node importedNode = importer.importNode(paragraph, true);
     dstDoc.getFirstSection().getBody().appendChild(importedNode);
 }

 dstDoc.updateListLabels();

 if (keepSourceNumbering) {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 } else {
     Assert.assertEquals(
             "6. Item 1\r\n" +
                     "7. Item 2 \r\n" +
                     "8. Item 3\r\n" +
                     "9. Item 4\r\n" +
                     "10. Item 1\r\n" +
                     "11. Item 2 \r\n" +
                     "12. Item 3\r\n" +
                     "13. Item 4", dstDoc.getFirstSection().getBody().toString(SaveFormat.TEXT).trim());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que especifica cómo se importará la numeración cuando haya conflictos entre los documentos de origen y destino. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es false.

 **Examples:** 

Muestra cómo fusionar listas de un documento.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. |

### setResolveThemeColors(boolean value) {#setResolveThemeColors-boolean}
```
public void setResolveThemeColors(boolean value)
```


Establece un valor booleano que especifica si se deben resolver forzosamente los colores de tema de las formas. El valor predeterminado es false.

 **Remarks:** 

Tenga en cuenta que esta opción solo es relevante para el modo [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Normalmente, Aspose.Words no resuelve los colores de tema de origen al importar estilos que pueden preservarse sin expandir los atributos de formato en atributos directos. Sin embargo, en este caso los colores reales de las formas importadas pueden diferir de los que tenían en el documento original. La razón es que los colores de tema difieren entre los documentos de origen y destino. Establecer esta opción en true obliga a resolver los colores de tema de las formas de origen y, por lo tanto, a preservar el color real de las formas que tienen en el documento de origen.

 **Examples:** 

Muestra cómo importar un nodo resolviendo los colores de tema de origen de las formas.

```

 Document srcDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(srcDoc);

 // Move to the primary footer and insert a shape that uses theme colors.
 builder.moveToHeaderFooter(HeaderFooterType.FOOTER_PRIMARY);
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 100.0, 50.0);
 shape.getStroke().setForeThemeColor(ThemeColor.DARK_1);

 Document dstDoc = new Document();
 // Import the source footer into the destination document with theme colors resolved,
 // so the shape preserves its actual color from the source document.
 HeaderFooter footer = srcDoc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 ImportFormatOptions options = new ImportFormatOptions();
 options.setResolveThemeColors(true);
 HeaderFooter importedFooter = (HeaderFooter)dstDoc.importNode(footer, true, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.getFirstSection().getHeadersFooters().add(importedFooter);

 dstDoc.save(getArtifactsDir() + "DocumentBase.ImportNodeWithResolveThemeColors.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que especifica si se deben resolver forzosamente los colores de tema de las formas. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es false.

 **Remarks:** 

Cuando esta opción está **enabled**, el estilo de origen se expandirá en atributos directos dentro del documento de destino, si se usa el modo de importación [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING).

Cuando esta opción está **disabled**, el estilo de origen se expandirá solo si está numerado. Los atributos existentes del destino no se sobrescribirán, incluidas las listas.

 **Examples:** 

Muestra cómo resolver estilos duplicados al insertar documentos.

```

 Document dstDoc = new Document();
 DocumentBuilder builder = new DocumentBuilder(dstDoc);

 Style myStyle = builder.getDocument().getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 // Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
 // If we insert the clone into the original document, the two styles with the same name will cause a clash.
 Document srcDoc = dstDoc.deepClone();
 srcDoc.getStyles().get("MyStyle").getFont().setColor(Color.RED);

 // When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
 // Aspose.Words will resolve style clashes by converting source document styles.
 // with the same names as destination styles into direct paragraph attributes.
 ImportFormatOptions options = new ImportFormatOptions();
 options.setSmartStyleBehavior(true);

 builder.insertDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, options);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.SmartStyleBehavior.docx");
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. |

