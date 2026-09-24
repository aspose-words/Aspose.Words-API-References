---
title: "FieldDde"
linktitle: "FieldDde"
second_title: "Aspose.Words para Java"
description: "Implementa el campo DDE en Java."
type: docs
weight: 221
url: /es/java/com.aspose.words/fielddde/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldDde extends Field
```

Implementa el campo DDE.

Para obtener más información, visite el artículo de documentación [ Working with Fields ][Working with Fields].

 **Remarks:** 

Para información copiada de otra aplicación, este campo vincula esa información a su archivo fuente original usando DDE.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Métodos

| Método | Descripción |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Obtiene si se debe actualizar este campo automáticamente. |
| [getDisplayResult()](#getDisplayResult) | Obtiene el texto que representa el resultado del campo mostrado. |
| [getEnd()](#getEnd) | Obtiene el nodo que representa el final del campo. |
| [getFieldCode()](#getFieldCode) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [getFormat()](#getFormat) | Obtiene un objeto [FieldFormat](../../com.aspose.words/fieldformat/) que proporciona acceso tipado al formato del campo. |
| [getInsertAsBitmap()](#getInsertAsBitmap) | Obtiene si se debe insertar el objeto enlazado como mapa de bits. |
| [getInsertAsHtml()](#getInsertAsHtml) | Obtiene si se debe insertar el objeto enlazado como texto con formato HTML. |
| [getInsertAsPicture()](#getInsertAsPicture) | Obtiene si se debe insertar el objeto enlazado como imagen. |
| [getInsertAsRtf()](#getInsertAsRtf) | Obtiene si se debe insertar el objeto enlazado en formato de texto enriquecido (RTF). |
| [getInsertAsText()](#getInsertAsText) | Obtiene si se debe insertar el objeto enlazado en formato solo texto. |
| [getInsertAsUnicode()](#getInsertAsUnicode) | Obtiene si se debe insertar el objeto enlazado como texto Unicode. |
| [getLocaleId()](#getLocaleId) | Obtiene el LCID del campo. |
| [getProgId()](#getProgId) | Obtiene el tipo de aplicación de la información del enlace. |
| [getResult()](#getResult) | Obtiene el texto que está entre el separador del campo y el final del campo. |
| [getSeparator()](#getSeparator) | Obtiene el nodo que representa el separador de campo. |
| [getSourceFullName()](#getSourceFullName) | Obtiene el nombre y la ubicación del archivo fuente. |
| [getSourceItem()](#getSourceItem) | Obtiene la parte del archivo fuente que se está vinculando. |
| [getStart()](#getStart) | Obtiene el nodo que representa el inicio del campo. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Obtiene el tipo de campo de Microsoft Word. |
| [isDirty()](#isDirty) | Obtiene si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [isDirty(boolean value)](#isDirty-boolean) | Establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [isLinked()](#isLinked) | Obtiene si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [isLinked(boolean value)](#isLinked-boolean) | Establece si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [isLocked()](#isLocked) | Obtiene si el campo está bloqueado (no debe recalcular su resultado). |
| [isLocked(boolean value)](#isLocked-boolean) | Establece si el campo está bloqueado (no debe recalcular su resultado). |
| [remove()](#remove) | Elimina el campo del documento. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Establece si se debe actualizar este campo automáticamente. |
| [setInsertAsBitmap(boolean value)](#setInsertAsBitmap-boolean) | Establece si se debe insertar el objeto vinculado como un mapa de bits. |
| [setInsertAsHtml(boolean value)](#setInsertAsHtml-boolean) | Establece si se debe insertar el objeto vinculado como texto con formato HTML. |
| [setInsertAsPicture(boolean value)](#setInsertAsPicture-boolean) | Establece si se debe insertar el objeto vinculado como una imagen. |
| [setInsertAsRtf(boolean value)](#setInsertAsRtf-boolean) | Establece si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF). |
| [setInsertAsText(boolean value)](#setInsertAsText-boolean) | Establece si se debe insertar el objeto vinculado en formato solo texto. |
| [setInsertAsUnicode(boolean value)](#setInsertAsUnicode-boolean) | Establece si se debe insertar el objeto vinculado como texto Unicode. |
| [setLocaleId(int value)](#setLocaleId-int) | Establece el LCID del campo. |
| [setProgId(String value)](#setProgId-java.lang.String) | Establece el tipo de aplicación de la información del enlace. |
| [setResult(String value)](#setResult-java.lang.String) | Establece el texto que está entre el separador de campo y el final del campo. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Establece el nombre y la ubicación del archivo fuente. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Establece la parte del archivo fuente que se está vinculando. |
| [unlink()](#unlink) | Ejecuta la desvinculación del campo. |
| [update()](#update) | Ejecuta la actualización del campo. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Ejecuta una actualización del campo. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Obtiene si se debe actualizar este campo automáticamente.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe actualizar este campo automáticamente.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Obtiene el texto que representa el resultado del campo mostrado.

 **Remarks:** 

El método [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) debe llamarse para obtener el valor correcto de los campos [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) y [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/).

 **Examples:** 

Muestra cómo obtener el texto real que un campo muestra en el documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("This document was written by ");
 FieldAuthor fieldAuthor = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);
 fieldAuthor.setAuthorName("John Doe");

 // We can use the DisplayResult property to verify what exact text
 // a field would display in its place in the document.
 Assert.assertEquals("", fieldAuthor.getDisplayResult());

 // Fields do not maintain accurate result values in real-time.
 // To make sure our fields display accurate results at any given time,
 // such as right before a save operation, we need to update them manually.
 fieldAuthor.update();

 Assert.assertEquals("John Doe", fieldAuthor.getDisplayResult());

 doc.save(getArtifactsDir() + "Field.DisplayResult.docx");
 
```

**Returns:**
java.lang.String - El texto que representa el resultado del campo mostrado.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Obtiene el nodo que representa el final del campo.

 **Examples:** 

Muestra cómo trabajar con una colección de campos.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldEnd](../../com.aspose.words/fieldend/) - The node that represents the field end.
### getFieldCode() {#getFieldCode}
```
public String getFieldCode()
```


Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código del campo como el resultado del campo de los campos secundarios.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Muestra cómo obtener el código de campo de un campo.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Returns:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador).

 **Examples:** 

Muestra cómo obtener el código de campo de un campo.

```

 // Open a document which contains a MERGEFIELD inside an IF field.
 Document doc = new Document(getMyDir() + "Nested fields.docx");
 FieldIf fieldIf = (FieldIf) doc.getRange().getFields().get(0);

 // There are two ways of getting a field's field code:
 // 1 -  Omit its inner fields:
 Assert.assertEquals(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.getFieldCode(false));

 // 2 -  Include its inner fields:
 Assert.assertEquals(" IF  MERGEFIELD NetIncome  > 0 \" (surplus of  MERGEFIELD  NetIncome \\f $ ) \" \"\" ",
         fieldIf.getFieldCode(true));

 // By default, the GetFieldCode method displays inner fields.
 Assert.assertEquals(fieldIf.getFieldCode(), fieldIf.getFieldCode(true));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true  si los códigos de campo secundarios deben incluirse. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Obtiene un objeto [FieldFormat](../../com.aspose.words/fieldformat/) que proporciona acceso tipado al formato del campo.

 **Examples:** 

Muestra cómo formatear los resultados del campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

**Returns:**
[FieldFormat](../../com.aspose.words/fieldformat/) - A [FieldFormat](../../com.aspose.words/fieldformat/) object that provides typed access to field's formatting.
### getInsertAsBitmap() {#getInsertAsBitmap}
```
public boolean getInsertAsBitmap()
```


Obtiene si se debe insertar el objeto enlazado como mapa de bits.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado como un mapa de bits.
### getInsertAsHtml() {#getInsertAsHtml}
```
public boolean getInsertAsHtml()
```


Obtiene si se debe insertar el objeto enlazado como texto con formato HTML.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado como texto con formato HTML.
### getInsertAsPicture() {#getInsertAsPicture}
```
public boolean getInsertAsPicture()
```


Obtiene si se debe insertar el objeto enlazado como imagen.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado como una imagen.
### getInsertAsRtf() {#getInsertAsRtf}
```
public boolean getInsertAsRtf()
```


Obtiene si se debe insertar el objeto enlazado en formato de texto enriquecido (RTF).

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF).
### getInsertAsText() {#getInsertAsText}
```
public boolean getInsertAsText()
```


Obtiene si se debe insertar el objeto enlazado en formato solo texto.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado en formato solo texto.
### getInsertAsUnicode() {#getInsertAsUnicode}
```
public boolean getInsertAsUnicode()
```


Obtiene si se debe insertar el objeto enlazado como texto Unicode.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe insertar el objeto vinculado como texto Unicode.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Obtiene el LCID del campo.

 **Examples:** 

Muestra cómo insertar un campo y trabajar con su configuración regional.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Returns:**
int - El LCID del campo.
### getProgId() {#getProgId}
```
public String getProgId()
```


Obtiene el tipo de aplicación de la información del enlace.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
java.lang.String - El tipo de aplicación de la información del enlace.
### getResult() {#getResult}
```
public String getResult()
```


Obtiene el texto que está entre el separador del campo y el final del campo.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Texto que está entre el separador de campo y el final del campo.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Obtiene el nodo que representa el separador de campo. Puede ser  null .

 **Examples:** 

Muestra cómo trabajar con una colección de campos.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldSeparator](../../com.aspose.words/fieldseparator/) - The node that represents the field separator.
### getSourceFullName() {#getSourceFullName}
```
public String getSourceFullName()
```


Obtiene el nombre y la ubicación del archivo fuente.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
java.lang.String - El nombre y la ubicación del archivo fuente.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Obtiene la parte del archivo fuente que se está vinculando.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
java.lang.String - La parte del archivo fuente que se está vinculando.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Obtiene el nodo que representa el inicio del campo.

 **Examples:** 

Muestra cómo trabajar con una colección de campos.

```

 public void fieldCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
     builder.insertField(" TIME ");
     builder.insertField(" REVNUM ");
     builder.insertField(" AUTHOR  \"John Doe\" ");
     builder.insertField(" SUBJECT \"My Subject\" ");
     builder.insertField(" QUOTE \"Hello world!\" ");
     doc.updateFields();

     FieldCollection fields = doc.getRange().getFields();

     Assert.assertEquals(6, fields.getCount());

     // Iterate over the field collection, and print contents and type
     // of every field using a custom visitor implementation.
     FieldVisitor fieldVisitor = new FieldVisitor();

     Iterator fieldEnumerator = fields.iterator();

     while (fieldEnumerator.hasNext()) {
         if (fieldEnumerator != null) {
             Field currentField = fieldEnumerator.next();

             currentField.getStart().accept(fieldVisitor);
             if (currentField.getSeparator() != null) {
                 currentField.getSeparator().accept(fieldVisitor);
             }
             currentField.getEnd().accept(fieldVisitor);
         } else {
             System.out.println("There are no fields in the document.");
         }
     }

     System.out.println(fieldVisitor.getText());
 }

 /// 
 /// Document visitor implementation that prints field info.
 /// 
 public static class FieldVisitor extends DocumentVisitor {
     public FieldVisitor() {
         mBuilder = new StringBuilder();
     }

     /// 
     /// Gets the plain text of the document that was accumulated by the visitor.
     /// 
     public String getText() {
         return mBuilder.toString();
     }

     /// 
     /// Called when a FieldStart node is encountered in the document.
     /// 
     public int visitFieldStart(final FieldStart fieldStart) {
         mBuilder.append("Found field: " + fieldStart.getFieldType() + "\r\n");
         mBuilder.append("\tField code: " + fieldStart.getField().getFieldCode() + "\r\n");
         mBuilder.append("\tDisplayed as: " + fieldStart.getField().getResult() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldSeparator node is encountered in the document.
     /// 
     public int visitFieldSeparator(final FieldSeparator fieldSeparator) {
         mBuilder.append("\tFound separator: " + fieldSeparator.getText() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) {
         mBuilder.append("End of field: " + fieldEnd.getFieldType() + "\r\n");

         return VisitorAction.CONTINUE;
     }

     private final  StringBuilder mBuilder;
 }
 
```

**Returns:**
[FieldStart](../../com.aspose.words/fieldstart/) - The node that represents the start of the field.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String}
```
public int getSwitchType(String switchName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Obtiene el tipo de campo de Microsoft Word.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - El tipo de campo de Microsoft Word. El valor devuelto es una de las constantes [FieldType](../../com.aspose.words/fieldtype/).
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Obtiene si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.

 **Examples:** 

Muestra cómo usar la propiedad especial para actualizar el resultado del campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Returns:**
boolean - Si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento.

 **Examples:** 

Muestra cómo usar la propiedad especial para actualizar el resultado del campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Give the document's built-in "Author" property value, and then display it with a field.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 FieldAuthor field = (FieldAuthor) builder.insertField(FieldType.FIELD_AUTHOR, true);

 Assert.assertFalse(field.isDirty());
 Assert.assertEquals("John Doe", field.getResult());

 // Update the property. The field still displays the old value.
 doc.getBuiltInDocumentProperties().setAuthor("John & Jane Doe");

 Assert.assertEquals("John Doe", field.getResult());

 // Since the field's value is out of date, we can mark it as "dirty".
 // This value will stay out of date until we update the field manually with the Field.Update() method.
 field.isDirty(true);

 // If we save without calling an update method,
 // the field will keep displaying the out of date value in the output document.
 doc.save(getArtifactsDir() + "Filed.UpdateDirtyFields.docx");

 // The LoadOptions object has an option to update all fields
 // marked as "dirty" when loading the document.
 LoadOptions options = new LoadOptions();
 options.setUpdateDirtyFields(updateDirtyFields);

 doc = new Document(getArtifactsDir() + "Filed.UpdateDirtyFields.docx", options);

 Assert.assertEquals("John & Jane Doe", doc.getBuiltInDocumentProperties().getAuthor());

 field = (FieldAuthor) doc.getRange().getFields().get(0);

 // Updating dirty fields like this automatically set their "IsDirty" flag to false.
 if (updateDirtyFields) {
     Assert.assertEquals("John & Jane Doe", field.getResult());
     Assert.assertFalse(field.isDirty());
 } else {
     Assert.assertEquals("John Doe", field.getResult());
     Assert.assertTrue(field.isDirty());
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |

### isLinked() {#isLinked}
```
public boolean isLinked()
```


Obtiene si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Returns:**
boolean - Si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento.
### isLinked(boolean value) {#isLinked-boolean}
```
public void isLinked(boolean value)
```


Establece si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe reducir el tamaño del archivo al no almacenar datos gráficos con el documento. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Obtiene si el campo está bloqueado (no debe recalcular su resultado).

 **Examples:** 

Muestra cómo trabajar con un nodo FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Returns:**
boolean - Si el campo está bloqueado (no debe recalcular su resultado).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Establece si el campo está bloqueado (no debe recalcular su resultado).

 **Examples:** 

Muestra cómo trabajar con un nodo FieldStart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldDate field = (FieldDate) builder.insertField(FieldType.FIELD_DATE, true);
 field.getFormat().setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 FieldChar fieldStart = field.getStart();

 Assert.assertEquals(FieldType.FIELD_DATE, fieldStart.getFieldType());
 Assert.assertEquals(false, fieldStart.isDirty());
 Assert.assertEquals(false, fieldStart.isLocked());

 // Retrieve the facade object which represents the field in the document.
 field = (FieldDate) fieldStart.getField();

 Assert.assertEquals(false, field.isLocked());
 Assert.assertEquals(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());

 // Update the field to show the current date.
 field.update();
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si el campo está bloqueado (no debe recalcular su resultado). |

### remove() {#remove}
```
public Node remove()
```


Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve  null .

 **Examples:** 

Muestra cómo eliminar campos de una colección de campos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.insertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
 builder.insertField(" TIME ");
 builder.insertField(" REVNUM ");
 builder.insertField(" AUTHOR  \"John Doe\" ");
 builder.insertField(" SUBJECT \"My Subject\" ");
 builder.insertField(" QUOTE \"Hello world!\" ");
 doc.updateFields();

 FieldCollection fields = doc.getRange().getFields();

 Assert.assertEquals(6, fields.getCount());

 // Below are four ways of removing fields from a field collection.
 // 1 -  Get a field to remove itself:
 fields.get(0).remove();
 Assert.assertEquals(5, fields.getCount());

 // 2 -  Get the collection to remove a field that we pass to its removal method:
 Field lastField = fields.get(3);
 fields.remove(lastField);
 Assert.assertEquals(4, fields.getCount());

 // 3 -  Remove a field from a collection at an index:
 fields.removeAt(2);
 Assert.assertEquals(3, fields.getCount());

 // 4 -  Remove all the fields from the collection at once:
 fields.clear();
 Assert.assertEquals(0, fields.getCount());
 
```

Muestra cómo procesar campos PRIVATE.

```

 public void fieldPrivate() throws Exception {
     // Open a Corel WordPerfect document which we have converted to .docx format.
     Document doc = new Document(getMyDir() + "Field sample - PRIVATE.docx");

     // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
     // Microsoft Word preserves PRIVATE fields during load/save operations,
     // but provides no functionality for them.
     FieldPrivate field = (FieldPrivate) doc.getRange().getFields().get(0);

     Assert.assertEquals(" PRIVATE \"My value\" ", field.getFieldCode());
     Assert.assertEquals(FieldType.FIELD_PRIVATE, field.getType());

     // We can also insert PRIVATE fields using a document builder.
     DocumentBuilder builder = new DocumentBuilder(doc);
     builder.insertField(FieldType.FIELD_PRIVATE, true);

     // These fields are not a viable way of protecting sensitive information.
     // Unless backward compatibility with older versions of WordPerfect is essential,
     // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
     Assert.assertEquals(2, doc.getRange().getFields().getCount());

     FieldPrivateRemover remover = new FieldPrivateRemover();
     doc.accept(remover);

     Assert.assertEquals(remover.getFieldsRemovedCount(), 2);
     Assert.assertEquals(doc.getRange().getFields().getCount(), 0);
 }

 /// 
 /// Removes all encountered PRIVATE fields.
 /// 
 public static class FieldPrivateRemover extends DocumentVisitor {
     public FieldPrivateRemover() {
         mFieldsRemovedCount = 0;
     }

     public int getFieldsRemovedCount() {
         return mFieldsRemovedCount;
     }

     /// 
     /// Called when a FieldEnd node is encountered in the document.
     /// If the node belongs to a PRIVATE field, the entire field is removed.
     /// 
     public int visitFieldEnd(final FieldEnd fieldEnd) throws Exception {
         if (fieldEnd.getFieldType() == FieldType.FIELD_PRIVATE) {
             fieldEnd.getField().remove();
             mFieldsRemovedCount++;
         }

         return VisitorAction.CONTINUE;
     }

     private int mFieldsRemovedCount;
 }
 
```

**Returns:**
[Node](../../com.aspose.words/node/)
### setAutoUpdate(boolean value) {#setAutoUpdate-boolean}
```
public void setAutoUpdate(boolean value)
```


Establece si se debe actualizar este campo automáticamente.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe actualizar este campo automáticamente. |

### setInsertAsBitmap(boolean value) {#setInsertAsBitmap-boolean}
```
public void setInsertAsBitmap(boolean value)
```


Establece si se debe insertar el objeto vinculado como un mapa de bits.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado como un mapa de bits. |

### setInsertAsHtml(boolean value) {#setInsertAsHtml-boolean}
```
public void setInsertAsHtml(boolean value)
```


Establece si se debe insertar el objeto vinculado como texto con formato HTML.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado como texto en formato HTML. |

### setInsertAsPicture(boolean value) {#setInsertAsPicture-boolean}
```
public void setInsertAsPicture(boolean value)
```


Establece si se debe insertar el objeto vinculado como una imagen.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado como una imagen. |

### setInsertAsRtf(boolean value) {#setInsertAsRtf-boolean}
```
public void setInsertAsRtf(boolean value)
```


Establece si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF).

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado en formato de texto enriquecido (RTF). |

### setInsertAsText(boolean value) {#setInsertAsText-boolean}
```
public void setInsertAsText(boolean value)
```


Establece si se debe insertar el objeto vinculado en formato solo texto.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado en formato solo texto. |

### setInsertAsUnicode(boolean value) {#setInsertAsUnicode-boolean}
```
public void setInsertAsUnicode(boolean value)
```


Establece si se debe insertar el objeto vinculado como texto Unicode.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe insertar el objeto vinculado como texto Unicode. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Establece el LCID del campo.

 **Examples:** 

Muestra cómo insertar un campo y trabajar con su configuración regional.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a DATE field, and then print the date it will display.
 // Your thread's current culture determines the formatting of the date.
 Field field = builder.insertField("DATE");
 System.out.println(MessageFormat.format("Today''s date, as displayed in the \"{0}\" culture: {1}", Locale.getDefault().getDisplayLanguage(), field.getResult()));

 Assert.assertEquals(1033, field.getLocaleId());
 // Changing the culture of our thread will impact the result of the DATE field.
 // Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
 // This way allows us to avoid changing the thread's culture to get this effect.
 doc.getFieldOptions().setFieldUpdateCultureSource(FieldUpdateCultureSource.FIELD_CODE);
 CultureInfo de = new CultureInfo("de-DE");
 field.setLocaleId(1031);
 field.update();

 System.out.println(MessageFormat.format("Today''s date, as displayed according to the \"{0}\" culture: {1}", Locale.forLanguageTag(LocaleUtil.getLocaleFromLCID(field.getLocaleId())).getDisplayLanguage(), field.getResult()));
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El LCID del campo. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


Establece el tipo de aplicación de la información del enlace.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El tipo de aplicación de la información del enlace. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Establece el texto que está entre el separador de campo y el final del campo.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando un código de campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Texto que está entre el separador de campo y el final del campo. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Establece el nombre y la ubicación del archivo fuente.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre y la ubicación del archivo fuente. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Establece la parte del archivo fuente que se está vinculando.

 **Examples:** 

Muestra cómo usar varios tipos de campo para enlazar a otros documentos en el sistema de archivos local y mostrar su contenido.

```

 public void fieldLinkedObjectsAsText(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of text.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Word.Document.8", getMyDir() + "Document.docx", null, true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.docx");
 }

 public static Object[][] fieldLinkedObjectsAsTextDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.TEXT},
                     {InsertLinkedObjectAs.UNICODE},
                     {InsertLinkedObjectAs.HTML},
                     {InsertLinkedObjectAs.RTF},
             };
 }

 public void fieldLinkedObjectsAsImage(int insertLinkedObjectAs) throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are three types of fields we can use to display contents from a linked document in the form of an image.
     // 1 -  A LINK field:
     builder.writeln("FieldLink:\n");
     insertFieldLink(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "MySpreadsheet.xlsx",
             "Sheet1!R2C2", true);

     // 2 -  A DDE field:
     builder.writeln("FieldDde:\n");
     insertFieldDde(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true, true);

     // 3 -  A DDEAUTO field:
     builder.writeln("FieldDdeAuto:\n");
     insertFieldDdeAuto(builder, insertLinkedObjectAs, "Excel.Sheet", getMyDir() + "Spreadsheet.xlsx",
             "Sheet1!R1C1", true);

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.LINK.DDE.DDEAUTO.AsImage.docx");
 }

 public static Object[][] fieldLinkedObjectsAsImageDataProvider() {
     return new Object[][]
             {
                     {InsertLinkedObjectAs.PICTURE},
                     {InsertLinkedObjectAs.BITMAP},
             };
 }

 /// 
 /// Use a document builder to insert a LINK field and set its properties according to parameters.
 /// 
 private void insertFieldLink(final DocumentBuilder builder, final int insertLinkedObjectAs,
                              final String progId, final String sourceFullName, final String sourceItem,
                              final boolean shouldAutoUpdate) throws Exception {
     FieldLink field = (FieldLink) builder.insertField(FieldType.FIELD_LINK, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDE field, and set its properties according to parameters.
 /// 
 private void insertFieldDde(final DocumentBuilder builder, final int insertLinkedObjectAs, final String progId,
                             final String sourceFullName, final String sourceItem, final boolean isLinked,
                             final boolean shouldAutoUpdate) throws Exception {
     FieldDde field = (FieldDde) builder.insertField(FieldType.FIELD_DDE, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setAutoUpdate(shouldAutoUpdate);
     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);

     builder.writeln("\n");
 }

 /// 
 /// Use a document builder to insert a DDEAUTO, field and set its properties according to parameters.
 /// 
 private void insertFieldDdeAuto(final DocumentBuilder builder, final int insertLinkedObjectAs,
                                 final String progId, final String sourceFullName, final String sourceItem,
                                 final boolean isLinked) throws Exception {
     FieldDdeAuto field = (FieldDdeAuto) builder.insertField(FieldType.FIELD_DDE_AUTO, true);

     switch (insertLinkedObjectAs) {
         case InsertLinkedObjectAs.TEXT:
             field.setInsertAsText(true);
             break;
         case InsertLinkedObjectAs.UNICODE:
             field.setInsertAsUnicode(true);
             break;
         case InsertLinkedObjectAs.HTML:
             field.setInsertAsHtml(true);
             break;
         case InsertLinkedObjectAs.RTF:
             field.setInsertAsRtf(true);
             break;
         case InsertLinkedObjectAs.PICTURE:
             field.setInsertAsPicture(true);
             break;
         case InsertLinkedObjectAs.BITMAP:
             field.setInsertAsBitmap(true);
             break;
     }

     field.setProgId(progId);
     field.setSourceFullName(sourceFullName);
     field.setSourceItem(sourceItem);
     field.isLinked(isLinked);
 }

 public final class InsertLinkedObjectAs {
     private InsertLinkedObjectAs() {
     }

     // LinkedObjectAsText
     public static final int TEXT = 0;
     public static final int UNICODE = 1;
     public static final int HTML = 2;
     public static final int RTF = 3;
     // LinkedObjectAsImage
     public static final int PICTURE = 4;
     public static final int BITMAP = 5;

     public static final int length = 6;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La parte del archivo fuente que se está vinculando. |

### unlink() {#unlink}
```
public boolean unlink()
```


Ejecuta la desvinculación del campo.

 **Remarks:** 

Reemplaza el campo con su resultado más reciente.

Algunos campos, como los campos XE (Entrada de índice) y SEQ (Secuencia), no pueden ser desvinculados.

 **Examples:** 

Muestra cómo desvincular un campo.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  si el campo ha sido desvinculado, de lo contrario  false .
### update() {#update}
```
public void update()
```


Realiza la actualización del campo. Lanza una excepción si el campo ya está siendo actualizado.

 **Examples:** 

Muestra cómo insertar un campo en un documento usando FieldType.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert two fields while passing a flag which determines whether to update them as the builder inserts them.
 // In some cases, updating fields could be computationally expensive, and it may be a good idea to defer the update.
 doc.getBuiltInDocumentProperties().setAuthor("John Doe");
 builder.write("This document was written by ");
 builder.insertField(FieldType.FIELD_AUTHOR, updateInsertedFieldsImmediately);

 builder.insertParagraph();
 builder.write("\nThis is page ");
 builder.insertField(FieldType.FIELD_PAGE, updateInsertedFieldsImmediately);

 Assert.assertEquals(" AUTHOR ", doc.getRange().getFields().get(0).getFieldCode());
 Assert.assertEquals(" PAGE ", doc.getRange().getFields().get(1).getFieldCode());

 if (updateInsertedFieldsImmediately) {
     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 } else {
     Assert.assertEquals("", doc.getRange().getFields().get(0).getResult());
     Assert.assertEquals("", doc.getRange().getFields().get(1).getResult());

     // We will need to update these fields using the update methods manually.
     doc.getRange().getFields().get(0).update();

     Assert.assertEquals("John Doe", doc.getRange().getFields().get(0).getResult());

     doc.updateFields();

     Assert.assertEquals("1", doc.getRange().getFields().get(1).getResult());
 }
 
```

Muestra cómo formatear los resultados del campo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```

### update(boolean ignoreMergeFormat) {#update-boolean}
```
public void update(boolean ignoreMergeFormat)
```


Realiza una actualización de campo. Lanza una excepción si el campo ya está siendo actualizado.

 **Examples:** 

Muestra cómo conservar o descartar los campos INCLUDEPICTURE al cargar un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 FieldIncludePicture includePicture = (FieldIncludePicture) builder.insertField(FieldType.FIELD_INCLUDE_PICTURE, true);
 includePicture.setSourceFullName(getImageDir() + "Transparent background logo.png");
 includePicture.update(true);

 try (ByteArrayOutputStream docStream = new ByteArrayOutputStream()) {
     doc.save(docStream, new OoxmlSaveOptions(SaveFormat.DOCX));

     // We can set a flag in a LoadOptions object to decide whether to convert all INCLUDEPICTURE fields
     // into image shapes when loading a document that contains them.
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setPreserveIncludePictureField(preserveIncludePictureField);
     }

     doc = new Document(new ByteArrayInputStream(docStream.toByteArray()), loadOptions);
     FieldCollection fieldCollection = doc.getRange().getFields();

     if (preserveIncludePictureField) {
         Assert.assertTrue(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));

         doc.updateFields();
         doc.save(getArtifactsDir() + "Field.PreserveIncludePicture.docx");
     } else {
         Assert.assertFalse(IterableUtils.matchesAny(fieldCollection, f -> f.getType() == FieldType.FIELD_INCLUDE_PICTURE));
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Si  true  entonces el formato directo del resultado del campo se abandona, sin importar el interruptor MERGEFORMAT, de lo contrario se realiza una actualización normal. |

