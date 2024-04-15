---
title: ImportFormatOptions
linktitle: ImportFormatOptions
second_title: Aspose.Words for Java
description: Allows to specify various import options to format output in Java.
type: docs
weight: 370
url: /java/com.aspose.words/importformatoptions/
---

**Inheritance:**
java.lang.Object
```
public class ImportFormatOptions
```

Allows to specify various import options to format output.

To learn more, visit the [ Specify Load Options ][Specify Load Options] documentation article.

 **Examples:** 

Shows how to resolve duplicate styles while inserting documents.

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
## Methods

| Method | Description |
| --- | --- |
| [getAdjustSentenceAndWordSpacing()](#getAdjustSentenceAndWordSpacing) | Gets a boolean value that specifies whether to adjust sentence and word spacing automatically. |
| [getForceCopyStyles()](#getForceCopyStyles) | Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode. |
| [getIgnoreHeaderFooter()](#getIgnoreHeaderFooter) | Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getIgnoreTextBoxes()](#getIgnoreTextBoxes) | Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |
| [getKeepSourceNumbering()](#getKeepSourceNumbering) | Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [getMergePastedLists()](#getMergePastedLists) | Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [getSmartStyleBehavior()](#getSmartStyleBehavior) | Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
| [setAdjustSentenceAndWordSpacing(boolean value)](#setAdjustSentenceAndWordSpacing-boolean) | Sets a boolean value that specifies whether to adjust sentence and word spacing automatically. |
| [setForceCopyStyles(boolean value)](#setForceCopyStyles-boolean) | Sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode. |
| [setIgnoreHeaderFooter(boolean value)](#setIgnoreHeaderFooter-boolean) | Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setIgnoreTextBoxes(boolean value)](#setIgnoreTextBoxes-boolean) | Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |
| [setKeepSourceNumbering(boolean value)](#setKeepSourceNumbering-boolean) | Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |
| [setMergePastedLists(boolean value)](#setMergePastedLists-boolean) | Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. |
| [setSmartStyleBehavior(boolean value)](#setSmartStyleBehavior-boolean) | Sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |
### getAdjustSentenceAndWordSpacing() {#getAdjustSentenceAndWordSpacing}
```
public boolean getAdjustSentenceAndWordSpacing()
```


Gets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is  false .

 **Examples:** 

Shows how to adjust sentence and word spacing automatically.

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
boolean - A boolean value that specifies whether to adjust sentence and word spacing automatically.
### getForceCopyStyles() {#getForceCopyStyles}
```
public boolean getForceCopyStyles()
```


Gets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode. The default value is  false .

 **Remarks:** 

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to  true , the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

 **Examples:** 

Shows how to copy source styles with unique names forcibly.

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
boolean - A boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode.
### getIgnoreHeaderFooter() {#getIgnoreHeaderFooter}
```
public boolean getIgnoreHeaderFooter()
```


Gets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

 **Examples:** 

Shows how to specifies ignoring or not source formatting of headers/footers content.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Returns:**
boolean - A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used.
### getIgnoreTextBoxes() {#getIgnoreTextBoxes}
```
public boolean getIgnoreTextBoxes()
```


Gets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

 **Examples:** 

Shows how to manage text box formatting while appending a document.

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
boolean - A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used.
### getKeepSourceNumbering() {#getKeepSourceNumbering}
```
public boolean getKeepSourceNumbering()
```


Gets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

 **Examples:** 

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

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

Shows how to import a document with numbered lists.

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

Shows how to resolve list numbering clashes in source and destination documents.

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
boolean - A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents.
### getMergePastedLists() {#getMergePastedLists}
```
public boolean getMergePastedLists()
```


Gets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

 **Examples:** 

Shows how to merge lists from a documents.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Returns:**
boolean - A boolean value that specifies whether pasted lists will be merged with surrounding lists.
### getSmartStyleBehavior() {#getSmartStyleBehavior}
```
public boolean getSmartStyleBehavior()
```


Gets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is  false .

 **Remarks:** 

When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

 **Examples:** 

Shows how to resolve duplicate styles while inserting documents.

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
boolean - A boolean value that specifies how styles will be imported when they have equal names in source and destination documents.
### setAdjustSentenceAndWordSpacing(boolean value) {#setAdjustSentenceAndWordSpacing-boolean}
```
public void setAdjustSentenceAndWordSpacing(boolean value)
```


Sets a boolean value that specifies whether to adjust sentence and word spacing automatically. The default value is  false .

 **Examples:** 

Shows how to adjust sentence and word spacing automatically.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies whether to adjust sentence and word spacing automatically. |

### setForceCopyStyles(boolean value) {#setForceCopyStyles-boolean}
```
public void setForceCopyStyles(boolean value)
```


Sets a boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode. The default value is  false .

 **Remarks:** 

By default, if a matching style already exists in a destination document, the source style formatting is expanded into direct node attributes and the style of this node is reset to a default.

When this option is set to  true , the source style will be forcibly copied into destination document with unique name and applied to the imported node.

Note, in this case it is not guaranteed that formatting of the imported node in destination document will be preserved.

 **Examples:** 

Shows how to copy source styles with unique names forcibly.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either to copy conflicting styles in [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode. |

### setIgnoreHeaderFooter(boolean value) {#setIgnoreHeaderFooter-boolean}
```
public void setIgnoreHeaderFooter(boolean value)
```


Sets a boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

 **Examples:** 

Shows how to specifies ignoring or not source formatting of headers/footers content.

```

 Document dstDoc = new Document(getMyDir() + "Document.docx");
 Document srcDoc = new Document(getMyDir() + "Header and footer types.docx");

 ImportFormatOptions importFormatOptions = new ImportFormatOptions();
 importFormatOptions.setIgnoreHeaderFooter(false);

 dstDoc.appendDocument(srcDoc, ImportFormatMode.KEEP_SOURCE_FORMATTING, importFormatOptions);

 dstDoc.save(getArtifactsDir() + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of headers/footers content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |

### setIgnoreTextBoxes(boolean value) {#setIgnoreTextBoxes-boolean}
```
public void setIgnoreTextBoxes(boolean value)
```


Sets a boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. The default value is  true .

 **Examples:** 

Shows how to manage text box formatting while appending a document.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies that source formatting of textboxes content ignored if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) mode is used. |

### setKeepSourceNumbering(boolean value) {#setKeepSourceNumbering-boolean}
```
public void setKeepSourceNumbering(boolean value)
```


Sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. The default value is  false .

 **Examples:** 

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

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

Shows how to import a document with numbered lists.

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

Shows how to resolve list numbering clashes in source and destination documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies how the numbering will be imported when it clashes in source and destination documents. |

### setMergePastedLists(boolean value) {#setMergePastedLists-boolean}
```
public void setMergePastedLists(boolean value)
```


Sets a boolean value that specifies whether pasted lists will be merged with surrounding lists. The default value is  false .

 **Examples:** 

Shows how to merge lists from a documents.

```

 Document srcDoc = new Document(getMyDir() + "List item.docx");
 Document dstDoc = new Document(getMyDir() + "List destination.docx");

 ImportFormatOptions options = new ImportFormatOptions(); { options.setMergePastedLists(true); }

 // Set the "MergePastedLists" property to "true" pasted lists will be merged with surrounding lists.
 dstDoc.appendDocument(srcDoc, ImportFormatMode.USE_DESTINATION_STYLES, options);

 dstDoc.save(getArtifactsDir() + "Document.MergePastedLists.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies whether pasted lists will be merged with surrounding lists. |

### setSmartStyleBehavior(boolean value) {#setSmartStyleBehavior-boolean}
```
public void setSmartStyleBehavior(boolean value)
```


Sets a boolean value that specifies how styles will be imported when they have equal names in source and destination documents. The default value is  false .

 **Remarks:** 

When this option is **enabled**, the source style will be expanded into a direct attributes inside a destination document, if [ImportFormatMode.KEEP\_SOURCE\_FORMATTING](../../com.aspose.words/importformatmode/\#KEEP-SOURCE-FORMATTING) importing mode is used.

When this option is **disabled**, the source style will be expanded only if it is numbered. Existing destination attributes will not be overridden, including lists.

 **Examples:** 

Shows how to resolve duplicate styles while inserting documents.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value that specifies how styles will be imported when they have equal names in source and destination documents. |

