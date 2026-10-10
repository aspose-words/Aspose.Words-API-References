---
title: "Range"
linktitle: "Range"
second_title: "Aspose.Words para Java"
description: "Representa un área contigua en un documento en Java."
type: docs
weight: 558
url: /es/java/com.aspose.words/range/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class Range implements Iterable
```

Representa un área contigua en un documento.

Para obtener más información, visite el artículo de documentación [ Working with Ranges ][Working with Ranges].

 **Remarks:** 

El documento está representado por un árbol de nodos y los nodos proporcionan operaciones para trabajar con el árbol, pero algunas operaciones son más fáciles de realizar si el documento se trata como una secuencia contigua de texto.

[Range](../../com.aspose.words/range/) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](../../com.aspose.words/range/) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

 **Examples:** 

Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Assert.assertEquals("Hello world!", doc.getRange().getText().trim());
 
```


[Working with Ranges]: https://docs.aspose.com/words/java/working-with-ranges/
## Métodos

| Método | Descripción |
| --- | --- |
| [delete()](#delete) | Elimina todos los caracteres del rango. |
| [getBookmarks()](#getBookmarks) | Devuelve una colección [getBookmarks()](../../com.aspose.words/range/\#getBookmarks) que representa todos los marcadores en el rango. |
| [getFields()](#getFields) | Devuelve una colección [getFields()](../../com.aspose.words/range/\#getFields) que representa todos los campos en el rango. |
| [getFormFields()](#getFormFields) | Devuelve una colección [getFormFields()](../../com.aspose.words/range/\#getFormFields) que representa todos los campos de formulario en el rango. |
| [getRevisions()](#getRevisions) | Obtiene una colección de revisiones (cambios controlados) que existen en este rango. |
| [getStructuredDocumentTags()](#getStructuredDocumentTags) | Devuelve una colección [getStructuredDocumentTags()](../../com.aspose.words/range/\#getStructuredDocumentTags) que representa todas las etiquetas estructuradas del documento en el rango. |
| [getText()](#getText) | Obtiene el texto del rango. |
| [iterator()](#iterator) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes) | Cambia los valores de tipo de campo [FieldChar.getFieldType()](../../com.aspose.words/fieldchar/\#getFieldType) de [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/) en este rango para que correspondan a los tipos de campo contenidos en los códigos de campo. |
| [replace(String pattern, String replacement)](#replace-java.lang.String-java.lang.String) | Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [replace(String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo. |
| [replace(Pattern pattern, String replacement)](#replace-java.util.regex.Pattern-java.lang.String) | Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [replace(Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena. |
| [toDocument()](#toDocument) | Construye un nuevo documento completamente formado que contiene el rango. |
| [unlinkFields()](#unlinkFields) | Desvincula los campos en este rango. |
| [updateFields()](#updateFields) | Actualiza los valores de los campos del documento en este rango. |
### delete() {#delete}
```
public void delete()
```


Elimina todos los caracteres del rango.

 **Examples:** 

Muestra cómo eliminar todos los nodos de un rango.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text to the first section in the document, and then add another section.
 builder.write("Section 1. ");
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.write("Section 2.");

 Assert.assertEquals("Section 1. \fSection 2.", doc.getText().trim());

 // Remove the first section entirely by removing all the nodes
 // within its range, including the section itself.
 doc.getSections().get(0).getRange().delete();

 Assert.assertEquals(1, doc.getSections().getCount());
 Assert.assertEquals("Section 2.", doc.getText().trim());
 
```

### getBookmarks() {#getBookmarks}
```
public BookmarkCollection getBookmarks()
```


Devuelve una colección [getBookmarks()](../../com.aspose.words/range/\#getBookmarks) que representa todos los marcadores en el rango.

 **Examples:** 

Muestra cómo agregar marcadores y actualizar su contenido.

```

 public void createUpdateAndPrintBookmarks() throws Exception {
     // Create a document with three bookmarks, then use a custom document visitor implementation to print their contents.
     Document doc = createDocumentWithBookmarks(3);
     BookmarkCollection bookmarks = doc.getRange().getBookmarks();
     printAllBookmarkInfo(bookmarks);

     // Bookmarks can be accessed in the bookmark collection by index or name, and their names can be updated.
     bookmarks.get(0).setName("{bookmarks[0].Name}_NewName");
     bookmarks.get("MyBookmark_2").setText("Updated text contents of {bookmarks[1].Name}");

     // Print all bookmarks again to see updated values.
     printAllBookmarkInfo(bookmarks);
 }

 /// 
 /// Create a document with a given number of bookmarks.
 /// 
 private static Document createDocumentWithBookmarks(int numberOfBookmarks) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     for (int i = 1; i <= numberOfBookmarks; i++) {
         String bookmarkName = "MyBookmark_" + i;

         builder.write("Text before bookmark.");
         builder.startBookmark(bookmarkName);
         builder.write(MessageFormat.format("Text inside {0}.", bookmarkName));
         builder.endBookmark(bookmarkName);
         builder.writeln("Text after bookmark.");
     }

     return doc;
 }

 /// 
 /// Use an iterator and a visitor to print info of every bookmark in the collection.
 /// 
 private static void printAllBookmarkInfo(BookmarkCollection bookmarks) throws Exception {
     BookmarkInfoPrinter bookmarkVisitor = new BookmarkInfoPrinter();

     // Get each bookmark in the collection to accept a visitor that will print its contents.
     Iterator enumerator = bookmarks.iterator();

     while (enumerator.hasNext()) {
         Bookmark currentBookmark = enumerator.next();

         if (currentBookmark != null) {
             currentBookmark.getBookmarkStart().accept(bookmarkVisitor);
             currentBookmark.getBookmarkEnd().accept(bookmarkVisitor);

             System.out.println(currentBookmark.getBookmarkStart().getText());
         }
     }
 }

 /// 
 /// Prints contents of every visited bookmark to the console.
 /// 
 public static class BookmarkInfoPrinter extends DocumentVisitor {
     public int visitBookmarkStart(BookmarkStart bookmarkStart) throws Exception {
         System.out.println(MessageFormat.format("BookmarkStart name: \"{0}\", Content: \"{1}\"", bookmarkStart.getName(),
                 bookmarkStart.getBookmark().getText()));
         return VisitorAction.CONTINUE;
     }

     public int visitBookmarkEnd(BookmarkEnd bookmarkEnd) {
         System.out.println(MessageFormat.format("BookmarkEnd name: \"{0}\"", bookmarkEnd.getName()));
         return VisitorAction.CONTINUE;
     }
 }
 
```

**Returns:**
[BookmarkCollection](../../com.aspose.words/bookmarkcollection/) - A [getBookmarks()](../../com.aspose.words/range/\#getBookmarks) collection that represents all bookmarks in the range.
### getFields() {#getFields}
```
public FieldCollection getFields()
```


Devuelve una colección [getFields()](../../com.aspose.words/range/\#getFields) que representa todos los campos en el rango.

 **Examples:** 

Muestra cómo personalizar el cambio de nodos con una devolución de llamada.

```

 public void fontChangeViaCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Set the node changing callback to custom implementation,
     // then add/remove nodes to get it to generate a log.
     HandleNodeChangingFontChanger callback = new HandleNodeChangingFontChanger();
     doc.setNodeChangingCallback(callback);

     builder.writeln("Hello world!");
     builder.writeln("Hello again!");
     builder.insertField(" HYPERLINK \"https://www.google.com/\" ");
     builder.insertShape(ShapeType.RECTANGLE, 300.0, 300.0);

     doc.getRange().getFields().get(0).remove();

     System.out.println(callback.getLog());
 }

 /// 
 /// Logs the date and time of each node insertion and removal.
 /// Sets a custom font name/size for the text contents of Run nodes.
 /// 
 public static class HandleNodeChangingFontChanger implements INodeChangingCallback {
     public void nodeInserted(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash:\t{0}", args.getNode().hashCode()));

         if (args.getNode().getNodeType() == NodeType.RUN) {
             Font font = ((Run) args.getNode()).getFont();
             mLog.append(MessageFormat.format("\tFont:\tChanged from \"{0}\" {1}pt", font.getName(), font.getSize()));

             font.setSize(24.0);
             font.setName("Arial");

             mLog.append(MessageFormat.format(" to \"{0}\" {1}pt", font.getName(), font.getSize()));
             mLog.append(MessageFormat.format("\tContents:\n\t\t\"{0}\"", args.getNode().getText()));
         }
     }

     public void nodeInserting(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode insertion:", new Date()));
     }

     public void nodeRemoved(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\tType:\t{0}", args.getNode().getNodeType()));
         mLog.append(MessageFormat.format("\tHash code:\t{0}", args.getNode().hashCode()));
     }

     public void nodeRemoving(NodeChangingArgs args) {
         mLog.append(MessageFormat.format("\n{0}\tNode removal:", new Date()));
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

**Returns:**
[FieldCollection](../../com.aspose.words/fieldcollection/) - A [getFields()](../../com.aspose.words/range/\#getFields) collection that represents all fields in the range.
### getFormFields() {#getFormFields}
```
public FormFieldCollection getFormFields()
```


Devuelve una colección [getFormFields()](../../com.aspose.words/range/\#getFormFields) que representa todos los campos de formulario en el rango.

 **Examples:** 

Muestra cómo insertar diferentes tipos de campos de formulario en un documento y procesarlos usando una implementación de visitante de documento.

```

 public void visitor() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Use a document builder to insert a combo box.
     builder.write("Choose a value from this combo box: ");
     FormField comboBox = builder.insertComboBox("MyComboBox", new String[]{"One", "Two", "Three"}, 0);
     comboBox.setCalculateOnExit(true);
     Assert.assertEquals(3, comboBox.getDropDownItems().getCount());
     Assert.assertEquals(0, comboBox.getDropDownSelectedIndex());
     Assert.assertTrue(comboBox.getEnabled());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert a check box.
     builder.write("Click this check box to tick/untick it: ");
     FormField checkBox = builder.insertCheckBox("MyCheckBox", false, 50);
     checkBox.isCheckBoxExactSize(true);
     checkBox.setHelpText("Right click to check this box");
     checkBox.setOwnHelp(true);
     checkBox.setStatusText("Checkbox status text");
     checkBox.setOwnStatus(true);
     Assert.assertEquals(50.0d, checkBox.getCheckBoxSize());
     Assert.assertFalse(checkBox.getChecked());
     Assert.assertFalse(checkBox.getDefault());

     builder.insertBreak(BreakType.PARAGRAPH_BREAK);

     // Use a document builder to insert text input form field.
     builder.write("Enter text here: ");
     FormField textInput = builder.insertTextInput("MyTextInput", TextFormFieldType.REGULAR, "", "Placeholder text", 50);
     textInput.setEntryMacro("EntryMacro");
     textInput.setExitMacro("ExitMacro");
     textInput.setTextInputDefault("Regular");
     textInput.setTextInputFormat("FIRST CAPITAL");
     textInput.setTextInputValue("New placeholder text");
     Assert.assertEquals(TextFormFieldType.REGULAR, textInput.getTextInputType());
     Assert.assertEquals(50, textInput.getMaxLength());

     // This collection contains all our form fields.
     FormFieldCollection formFields = doc.getRange().getFormFields();
     Assert.assertEquals(3, formFields.getCount());

     // Fields display our form fields. We can see their field codes by opening this document
     // in Microsoft and pressing Alt + F9. These fields have no switches,
     // and members of the FormField object fully govern their form fields' content.
     Assert.assertEquals(3, doc.getRange().getFields().getCount());
     Assert.assertEquals(" FORMDROPDOWN ", doc.getRange().getFields().get(0).getFieldCode());
     Assert.assertEquals(" FORMCHECKBOX ", doc.getRange().getFields().get(1).getFieldCode());
     Assert.assertEquals(" FORMTEXT ", doc.getRange().getFields().get(2).getFieldCode());

     // Allow each form field to accept a document visitor.
     FormFieldVisitor formFieldVisitor = new FormFieldVisitor();

     Iterator fieldEnumerator = formFields.iterator();
     while (fieldEnumerator.hasNext())
         fieldEnumerator.next().accept(formFieldVisitor);

     System.out.println(formFieldVisitor.getText());

     doc.updateFields();
     doc.save(getArtifactsDir() + "FormFields.Visitor.html");
 }

 /// 
 /// Visitor implementation that prints details of form fields that it visits.
 /// 
 public static class FormFieldVisitor extends DocumentVisitor {
     public FormFieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Called when a FormField node is encountered in the document.
     /// 
     public int visitFormField(FormField formField) {
         appendLine(formField.getType() + ": \"" + formField.getName() + "\"");
         appendLine("\tStatus: " + (formField.getEnabled() ? "Enabled" : "Disabled"));
         appendLine("\tHelp Text:  " + formField.getHelpText());
         appendLine("\tEntry macro name: " + formField.getEntryMacro());
         appendLine("\tExit macro name: " + formField.getExitMacro());

         switch (formField.getType()) {
             case FieldType.FIELD_FORM_DROP_DOWN:
                 appendLine("\tDrop down items count: " + formField.getDropDownItems().getCount() + ", default selected item index: " + formField.getDropDownSelectedIndex());
                 appendLine("\tDrop down items: " + String.join(", ", formField.getDropDownItems()));
                 break;
             case FieldType.FIELD_FORM_CHECK_BOX:
                 appendLine("\tCheckbox size: " + formField.getCheckBoxSize());
                 appendLine("\t" + "Checkbox is currently: " + (formField.getChecked() ? "checked, " : "unchecked, ") + "by default: " + (formField.getDefault() ? "checked" : "unchecked"));
                 break;
             case FieldType.FIELD_FORM_TEXT_INPUT:
                 appendLine("\tInput format: " + formField.getTextInputFormat());
                 appendLine("\tCurrent contents: " + formField.getResult());
                 break;
         }

         // Let the visitor continue visiting other nodes.
         return VisitorAction.CONTINUE;
     }

     /// 
     /// Adds newline char-terminated text to the current output.
     /// 
     private void appendLine(String text) {
         mBuilder.append(text + '\n');
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     private final StringBuilder mBuilder;
 }
 
```

**Returns:**
[FormFieldCollection](../../com.aspose.words/formfieldcollection/) - A [getFormFields()](../../com.aspose.words/range/\#getFormFields) collection that represents all form fields in the range.
### getRevisions() {#getRevisions}
```
public RevisionCollection getRevisions()
```


Obtiene una colección de revisiones (cambios controlados) que existen en este rango.

 **Remarks:** 

La colección devuelta es una colección "en vivo", lo que significa que si eliminas partes de un documento que contienen revisiones, las revisiones eliminadas desaparecerán automáticamente de esta colección.

 **Examples:** 

Muestra cómo trabajar con revisiones en un rango.

```

 Document doc = new Document(getMyDir() + "Revisions.docx");

 Paragraph paragraph = doc.getFirstSection().getBody().getFirstParagraph();
 for (Revision revision : paragraph.getRange().getRevisions())
 {
     if (revision.getRevisionType() == RevisionType.DELETION)
         revision.accept();
 }

 // Reject the first section revisions.
 doc.getFirstSection().getRange().getRevisions().rejectAll();
 
```

**Returns:**
[RevisionCollection](../../com.aspose.words/revisioncollection/) - A collection of revisions (tracked changes) that exist in this range.
### getStructuredDocumentTags() {#getStructuredDocumentTags}
```
public StructuredDocumentTagCollection getStructuredDocumentTags()
```


Devuelve una colección [getStructuredDocumentTags()](../../com.aspose.words/range/\#getStructuredDocumentTags) que representa todas las etiquetas estructuradas del documento en el rango.

 **Examples:** 

Muestra cómo eliminar una etiqueta de documento estructurado.

```

 Document doc = new Document(getMyDir() + "Structured document tags.docx");

 StructuredDocumentTagCollection structuredDocumentTags = doc.getRange().getStructuredDocumentTags();
 IStructuredDocumentTag sdt;
 for (int i = 0; i < structuredDocumentTags.getCount(); i++)
 {
     sdt = structuredDocumentTags.get(i);
     System.out.println(sdt.getTitle());
 }

 sdt = structuredDocumentTags.getById(1691867797);
 Assert.assertEquals(1691867797, sdt.getId());

 Assert.assertEquals(5, structuredDocumentTags.getCount());
 // Remove the structured document tag by Id.
 structuredDocumentTags.remove(1691867797);
 // Remove the structured document tag at position 0.
 structuredDocumentTags.removeAt(0);
 Assert.assertEquals(3, structuredDocumentTags.getCount());
 
```

**Returns:**
[StructuredDocumentTagCollection](../../com.aspose.words/structureddocumenttagcollection/) - A [getStructuredDocumentTags()](../../com.aspose.words/range/\#getStructuredDocumentTags) collection that represents all structured document tags in the range.
### getText() {#getText}
```
public String getText()
```


Obtiene el texto del rango.

 **Remarks:** 

La cadena devuelta incluye todos los caracteres de control y especiales según se describe en [ControlChar](../../com.aspose.words/controlchar/).

 **Examples:** 

Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Assert.assertEquals("Hello world!", doc.getRange().getText().trim());
 
```

**Returns:**
java.lang.String - El texto del rango.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### normalizeFieldTypes() {#normalizeFieldTypes}
```
public void normalizeFieldTypes()
```


Cambia los valores de tipo de campo [FieldChar.getFieldType()](../../com.aspose.words/fieldchar/\#getFieldType) de [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/) en este rango para que correspondan a los tipos de campo contenidos en los códigos de campo.

 **Remarks:** 

Utiliza este método después de cambios en el documento que afectan los tipos de campo.

Para cambiar los valores de tipo de campo en todo el documento, usa [Document.normalizeFieldTypes()](../../com.aspose.words/document/\#normalizeFieldTypes).

 **Examples:** 

Muestra cómo mantener actualizado el tipo de un campo con su código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field field = builder.insertField("DATE", null);

 // Aspose.Words automatically detects field types based on field codes.
 Assert.assertEquals(FieldType.FIELD_DATE, field.getType());

 // Manually change the raw text of the field, which determines the field code.
 Run fieldText = (Run) doc.getFirstSection().getBody().getFirstParagraph().getChildNodes(NodeType.RUN, true).get(0);
 fieldText.setText("PAGE");

 // Changing the field code has changed this field to one of a different type,
 // but the field's type properties still display the old type.
 Assert.assertEquals("PAGE", field.getFieldCode());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getStart().getFieldType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getSeparator().getFieldType());
 Assert.assertEquals(FieldType.FIELD_DATE, field.getEnd().getFieldType());

 // Update those properties with this method to display current value.
 doc.normalizeFieldTypes();

 Assert.assertEquals(FieldType.FIELD_PAGE, field.getType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getStart().getFieldType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getSeparator().getFieldType());
 Assert.assertEquals(FieldType.FIELD_PAGE, field.getEnd().getFieldType());
 
```

### replace(String pattern, String replacement) {#replace-java.lang.String-java.lang.String}
```
public int replace(String pattern, String replacement)
```


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

 **Remarks:** 

El patrón no se usará como expresión regular. Por favor, utiliza [replace(java.util.regex.Pattern, java.lang.String)](../../com.aspose.words/range/\#replace-java.util.regex.Pattern--java.lang.String) si necesitas expresiones regulares.

Se utilizó comparación sin distinción entre mayúsculas y minúsculas.

El método puede procesar saltos en tanto la cadena del patrón como la de reemplazo.

Debes usar metacaracteres especiales si necesitas trabajar con saltos:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break

Utiliza el método [replace(java.lang.String, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range/\#replace-java.lang.String--java.lang.String--com.aspose.words.FindReplaceOptions) para una personalización más flexible.

 **Examples:** 

Muestra cómo realizar una operación de buscar y reemplazar texto en el contenido de un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Greetings, _FullName_!");

 // Perform a find-and-replace operation on our document's contents and verify the number of replacements that took place.
 int replacementCount = doc.getRange().replace("_FullName_", "John Doe");

 Assert.assertEquals(1, replacementCount);
 Assert.assertEquals("Greetings, John Doe!", doc.getText().trim());
 
```

Muestra cómo agregar formato a los párrafos en los que una operación de buscar y reemplazar ha encontrado coincidencias.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
 builder.writeln("This one will not!");
 builder.write("This one also will.");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(2).getParagraphFormat().getAlignment());

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "Alignment" property to "ParagraphAlignment.Right" to right-align every paragraph
 // that contains a match that the find-and-replace operation finds.
 options.getApplyParagraphFormat().setAlignment(ParagraphAlignment.RIGHT);

 // Replace every full stop that is right before a paragraph break with an exclamation point.
 int count = doc.getRange().replace(".&p", "!&p", options);

 Assert.assertEquals(2, count);
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(0).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.LEFT, paragraphs.get(1).getParagraphFormat().getAlignment());
 Assert.assertEquals(ParagraphAlignment.RIGHT, paragraphs.get(2).getParagraphFormat().getAlignment());
 Assert.assertEquals("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
         "This one will not!\r" +
         "This one also will!", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public int replace(String pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo.

 **Remarks:** 

El patrón no se usará como expresión regular. Por favor, utiliza [replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range/\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions) si necesitas expresiones regulares.

El método puede procesar saltos en tanto la cadena del patrón como la de reemplazo.

Debes usar metacaracteres especiales si necesitas trabajar con saltos:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break
 *  **&&** \- & character

 **Examples:** 

Muestra cómo reemplazar texto en el pie de página de un documento.

```

 Document doc = new Document(getMyDir() + "Footer.docx");

 HeaderFooterCollection headersFooters = doc.getFirstSection().getHeadersFooters();
 HeaderFooter footer = headersFooters.getByHeaderFooterType(HeaderFooterType.FOOTER_PRIMARY);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setMatchCase(false);
 options.setFindWholeWordsOnly(false);

 int currentYear = Calendar.YEAR;
 footer.getRange().replace("(C) 2006 Aspose Pty Ltd.", MessageFormat.format("Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

 doc.save(getArtifactsDir() + "HeaderFooter.ReplaceText.docx");
 
```

Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Ruby bought a ruby necklace.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
 // Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
 options.setMatchCase(matchCase);

 doc.getRange().replace("Ruby", "Jade", options);

 Assert.assertEquals(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
         doc.getText().trim());
 
```

Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jackson will meet you in Jacksonville.");

 // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
 FindReplaceOptions options = new FindReplaceOptions();

 // Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
 // Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
 options.setFindWholeWordsOnly(findWholeWordsOnly);

 doc.getRange().replace("Jackson", "Louis", options);

 Assert.assertEquals(
         findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
         doc.getText().trim());
 
```

Muestra cómo reemplazar todas las instancias de una cadena de texto en una tabla y celda.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Carrots");
 builder.insertCell();
 builder.write("50");
 builder.endRow();
 builder.insertCell();
 builder.write("Potatoes");
 builder.insertCell();
 builder.write("50");
 builder.endTable();

 FindReplaceOptions options = new FindReplaceOptions();
 options.setMatchCase(true);
 options.setFindWholeWordsOnly(true);

 // Perform a find-and-replace operation on an entire table.
 table.getRange().replace("Carrots", "Eggs", options);

 // Perform a find-and-replace operation on the last cell of the last row of the table.
 table.getLastRow().getLastCell().getRange().replace("50", "20", options);

 Assert.assertEquals("Eggs50" +
                 "Potatoes20", table.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
int - El número de reemplazos realizados.
### replace(Pattern pattern, String replacement) {#replace-java.util.regex.Pattern-java.lang.String}
```
public int replace(Pattern pattern, String replacement)
```


Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena.

 **Remarks:** 

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar saltos en tanto la cadena del patrón como la de reemplazo.

Debes usar metacaracteres especiales si necesitas trabajar con saltos:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break

Utiliza el método [replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range/\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions) para una personalización más flexible.

 **Examples:** 

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otro texto.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

 doc.getRange().replace(Pattern.compile("gr(a|e)y"), "lavender");

 Assert.assertEquals("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.getText().trim());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replace(Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public int replace(Pattern pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las ocurrencias de un patrón de caracteres especificado por una expresión regular con otra cadena.

 **Remarks:** 

Reemplaza toda la coincidencia capturada por la expresión regular.

El método puede procesar saltos en tanto la cadena del patrón como la de reemplazo.

Debes usar metacaracteres especiales si necesitas trabajar con saltos:

 *  **&p** \- paragraph break
 *  **&b** \- section break
 *  **&m** \- page break
 *  **&l** \- manual line break
 *  **&&** \- & character

 **Examples:** 

Muestra cómo reemplazar todas las ocurrencias de un patrón de expresión regular con otra cadena, mientras se rastrean todos esos reemplazos.

```

 public void replaceWithCallback() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Our new location in New York City is opening tomorrow. " +
             "Hope to see all our NYC-based customers at the opening!");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();

     // Set a callback that tracks any replacements that the "Replace" method will make.
     TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
     options.setReplacingCallback(logger);

     doc.getRange().replace(Pattern.compile("New York City|NYC"), "Washington", options);

     Assert.assertEquals("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
             "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.getText().trim());

     Assert.assertEquals("\"New York City\" converted to \"Washington\" 20 characters into a 21 node." +
             "\"NYC\" converted to \"Washington\" 42 characters into a 21 node.", logger.getLog().trim());
 }

 /// 
 /// Maintains a log of every text replacement done by a find-and-replace operation
 /// and notes the original matched text's value.
 /// 
 private static class TextFindAndReplacementLogger implements IReplacingCallback {
     public int replacing(ReplacingArgs args) {
         mLog.append(MessageFormat.format("\"{0}\" converted to \"{1}\" {2} characters into a {3} node.", args.getMatch().group(0), args.getReplacement(), args.getMatchOffset(), args.getMatchNode().getNodeType()));

         args.setReplacement(MessageFormat.format("(Old value:\"{0}\") {1}", args.getMatch().group(0), args.getReplacement()));
         return ReplaceAction.REPLACE;
     }

     public String getLog() {
         return mLog.toString();
     }

     private final StringBuilder mLog = new StringBuilder();
 }
 
```

Muestra cómo insertar el contenido completo de un documento como reemplazo de una coincidencia en una operación de buscar y reemplazar.

```

 public void insertDocumentAtReplace() throws Exception {
     Document mainDoc = new Document(getMyDir() + "Document insertion destination.docx");

     // We can use a "FindReplaceOptions" object to modify the find-and-replace process.
     FindReplaceOptions options = new FindReplaceOptions();
     options.setReplacingCallback(new InsertDocumentAtReplaceHandler());

     mainDoc.getRange().replace(Pattern.compile("\[MY_DOCUMENT\]"), "", options);
     mainDoc.save(getArtifactsDir() + "InsertDocument.InsertDocumentAtReplace.docx");

 }

 private static class InsertDocumentAtReplaceHandler implements IReplacingCallback {
     public int replacing(ReplacingArgs args) throws Exception {
         Document subDoc = new Document(getMyDir() + "Document.docx");

         // Insert a document after the paragraph containing the matched text.
         Paragraph para = (Paragraph) args.getMatchNode().getParentNode();
         insertDocument(para, subDoc);

         // Remove the paragraph with the matched text.
         para.remove();

         return ReplaceAction.SKIP;
     }
 }

 /// 
 /// Inserts all the nodes of another document after a paragraph or table.
 /// 
 private static void insertDocument(Node insertionDestination, Document docToInsert) {
     if (((insertionDestination.getNodeType()) == (NodeType.PARAGRAPH)) || ((insertionDestination.getNodeType()) == (NodeType.TABLE))) {
         CompositeNode dstStory = insertionDestination.getParentNode();

         NodeImporter importer =
                 new NodeImporter(docToInsert, insertionDestination.getDocument(), ImportFormatMode.KEEP_SOURCE_FORMATTING);

         for (Section srcSection : docToInsert.getSections())
             for (Node srcNode : srcSection.getBody()) {
                 // Skip the node if it is the last empty paragraph in a section.
                 if (((srcNode.getNodeType()) == (NodeType.PARAGRAPH))) {
                     Paragraph para = (Paragraph) srcNode;
                     if (para.isEndOfSection() && !para.hasChildNodes())
                         continue;
                 }

                 Node newNode = importer.importNode(srcNode, true);

                 dstStory.insertAfter(newNode, insertionDestination);
                 insertionDestination = newNode;
             }
     } else {
         throw new IllegalArgumentException("The destination node must be either a paragraph or table.");
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
int - El número de reemplazos realizados.
### toDocument() {#toDocument}
```
public Document toDocument()
```


Construye un nuevo documento completamente formado que contiene el rango.

**Returns:**
[Document](../../com.aspose.words/document/)
### unlinkFields() {#unlinkFields}
```
public void unlinkFields()
```


Desvincula los campos en este rango.

 **Remarks:** 

Reemplaza todos los campos en este rango con sus resultados más recientes.

Para desvincular campos en todo el documento, usa [unlinkFields()](../../com.aspose.words/range/\#unlinkFields).

 **Examples:** 

Muestra cómo desvincular todos los campos en un rango.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");

 Section newSection = (Section) doc.getSections().get(0).deepClone(true);
 doc.getSections().add(newSection);

 doc.getSections().get(1).getRange().unlinkFields();
 
```

### updateFields() {#updateFields}
```
public void updateFields()
```


Actualiza los valores de los campos del documento en este rango.

 **Remarks:** 

Cuando abres, modificas y luego guardas un documento, Aspose.Words no actualiza los campos automáticamente, los mantiene intactos. Por lo tanto, normalmente querrás llamar a este método antes de guardar si has modificado el documento programáticamente y deseas asegurarte de que los valores de campo correctos (calculados) aparezcan en el documento guardado.

No es necesario actualizar los campos después de ejecutar una combinación de correspondencia porque la combinación de correspondencia es un tipo de actualización de campos y actualiza automáticamente todos los campos del documento.

Este método no actualiza todos los tipos de campo. Para la lista detallada de tipos de campo compatibles, consulta la Guía del Programador.

Este método no actualiza los campos que están relacionados con los algoritmos de diseño de página (p. ej., PAGE, PAGES, PAGEREF). Los campos relacionados con el diseño de página se actualizan cuando renderizas un documento o llamas a [Document.updatePageLayout()](../../com.aspose.words/document/\#updatePageLayout).

Para actualizar los campos en todo el documento, usa [Document.updateFields()](../../com.aspose.words/document/\#updateFields).

 **Examples:** 

Muestra cómo actualizar todos los campos en un rango.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DOCPROPERTY Category");
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.insertField(" DOCPROPERTY Category");

 // The above DOCPROPERTY fields will display the value of this built-in document property.
 doc.getBuiltInDocumentProperties().setCategory("MyCategory");

 // If we update the value of a document property, we will need to update all the DOCPROPERTY fields to display it.
 Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
 Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

 // Update all the fields that are in the range of the first section.
 doc.getFirstSection().getRange().updateFields();

 Assert.assertEquals("MyCategory", doc.getRange().getFields().get(0).getResult());
 Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());
 
```

