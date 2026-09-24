---
title: "FieldIncludeText"
linktitle: "FieldIncludeText"
second_title: "Aspose.Words para Java"
description: "Implementa el campo INCLUDETEXT en Java."
type: docs
weight: 248
url: /es/java/com.aspose.words/fieldincludetext/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldIncludeText extends Field
```

Implementa el campo INCLUDETEXT.

Para obtener más información, visite el artículo de documentación [ Working with Fields ][Working with Fields].

 **Remarks:** 

Inserta todo o parte del texto y los gráficos contenidos en otro documento.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Métodos

| Método | Descripción |
| --- | --- |
| [getBookmarkName()](#getBookmarkName) | Obtiene el nombre del marcador en el documento a incluir. |
| [getDisplayResult()](#getDisplayResult) | Obtiene el texto que representa el resultado del campo mostrado. |
| [getEncoding()](#getEncoding) | Obtiene la codificación aplicada a los datos dentro del archivo referenciado. |
| [getEnd()](#getEnd) | Obtiene el nodo que representa el final del campo. |
| [getFieldCode()](#getFieldCode) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Devuelve el texto entre el inicio del campo y el separador del campo (o el final del campo si no hay separador). |
| [getFormat()](#getFormat) | Obtiene un objeto [FieldFormat](../../com.aspose.words/fieldformat/) que proporciona acceso tipado al formato del campo. |
| [getLocaleId()](#getLocaleId) | Obtiene el LCID del campo. |
| [getLockFields()](#getLockFields) | Obtiene si se deben impedir que los campos en el documento incluido se actualicen. |
| [getMimeType()](#getMimeType) | Obtiene el tipo MIME del archivo referenciado. |
| [getNamespaceMappings()](#getNamespaceMappings) | Obtiene los mapeos de espacios de nombres para consultas XPath. |
| [getResult()](#getResult) | Obtiene el texto que está entre el separador del campo y el final del campo. |
| [getSeparator()](#getSeparator) | Obtiene el nodo que representa el separador de campo. |
| [getSourceFullName()](#getSourceFullName) | Obtiene la ubicación del documento usando un IRI. |
| [getStart()](#getStart) | Obtiene el nodo que representa el inicio del campo. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getTextConverter()](#getTextConverter) | Obtiene el nombre del convertidor de texto para el formato del archivo incluido. |
| [getType()](#getType) | Obtiene el tipo de campo de Microsoft Word. |
| [getXPath()](#getXPath) | Obtiene XPath para la porción deseada del archivo XML. |
| [getXslTransformation()](#getXslTransformation) | Obtiene la ubicación de la Transformación XSL para formatear datos XML. |
| [isDirty()](#isDirty) | Obtiene si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [isDirty(boolean value)](#isDirty-boolean) | Establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [isLocked()](#isLocked) | Obtiene si el campo está bloqueado (no debe recalcular su resultado). |
| [isLocked(boolean value)](#isLocked-boolean) | Establece si el campo está bloqueado (no debe recalcular su resultado). |
| [remove()](#remove) | Elimina el campo del documento. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String) | Establece el nombre del marcador en el documento a incluir. |
| [setEncoding(String value)](#setEncoding-java.lang.String) | Establece la codificación aplicada a los datos dentro del archivo referenciado. |
| [setLocaleId(int value)](#setLocaleId-int) | Establece el LCID del campo. |
| [setLockFields(boolean value)](#setLockFields-boolean) | Establece si se deben impedir que los campos en el documento incluido se actualicen. |
| [setMimeType(String value)](#setMimeType-java.lang.String) | Establece el tipo MIME del archivo referenciado. |
| [setNamespaceMappings(String value)](#setNamespaceMappings-java.lang.String) | Establece los mapeos de espacios de nombres para consultas XPath. |
| [setResult(String value)](#setResult-java.lang.String) | Establece el texto que está entre el separador de campo y el final del campo. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Establece la ubicación del documento usando un IRI. |
| [setTextConverter(String value)](#setTextConverter-java.lang.String) | Establece el nombre del convertidor de texto para el formato del archivo incluido. |
| [setXPath(String value)](#setXPath-java.lang.String) | Establece XPath para la porción deseada del archivo XML. |
| [setXslTransformation(String value)](#setXslTransformation-java.lang.String) | Establece la ubicación de la Transformación XSL para formatear datos XML. |
| [unlink()](#unlink) | Ejecuta la desvinculación del campo. |
| [update()](#update) | Ejecuta la actualización del campo. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Ejecuta una actualización del campo. |
### getBookmarkName() {#getBookmarkName}
```
public String getBookmarkName()
```


Obtiene el nombre del marcador en el documento a incluir.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - El nombre del marcador en el documento a incluir.
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
### getEncoding() {#getEncoding}
```
public String getEncoding()
```


Obtiene la codificación aplicada a los datos dentro del archivo referenciado.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - La codificación aplicada a los datos dentro del archivo referenciado.
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
### getLockFields() {#getLockFields}
```
public boolean getLockFields()
```


Obtiene si se deben impedir que los campos en el documento incluido se actualicen.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
boolean - Si se deben impedir que los campos en el documento incluido se actualicen.
### getMimeType() {#getMimeType}
```
public String getMimeType()
```


Obtiene el tipo MIME del archivo referenciado.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - El tipo MIME del archivo referenciado.
### getNamespaceMappings() {#getNamespaceMappings}
```
public String getNamespaceMappings()
```


Obtiene los mapeos de espacios de nombres para consultas XPath.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - Las asignaciones de espacio de nombres para consultas XPath.
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


Obtiene la ubicación del documento usando un IRI.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - La ubicación del documento usando un IRI.
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
### getTextConverter() {#getTextConverter}
```
public String getTextConverter()
```


Obtiene el nombre del convertidor de texto para el formato del archivo incluido.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - El nombre del convertidor de texto para el formato del archivo incluido.
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
### getXPath() {#getXPath}
```
public String getXPath()
```


Obtiene XPath para la porción deseada del archivo XML.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - XPath para la porción deseada del archivo XML.
### getXslTransformation() {#getXslTransformation}
```
public String getXslTransformation()
```


Obtiene la ubicación de la Transformación XSL para formatear datos XML.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Returns:**
java.lang.String - La ubicación de la Transformación XSL para formatear datos XML.
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
### setBookmarkName(String value) {#setBookmarkName-java.lang.String}
```
public void setBookmarkName(String value)
```


Establece el nombre del marcador en el documento a incluir.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del marcador en el documento a incluir. |

### setEncoding(String value) {#setEncoding-java.lang.String}
```
public void setEncoding(String value)
```


Establece la codificación aplicada a los datos dentro del archivo referenciado.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La codificación aplicada a los datos dentro del archivo referenciado. |

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

### setLockFields(boolean value) {#setLockFields-boolean}
```
public void setLockFields(boolean value)
```


Establece si se deben impedir que los campos en el documento incluido se actualicen.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Si se debe impedir que los campos en el documento incluido se actualicen. |

### setMimeType(String value) {#setMimeType-java.lang.String}
```
public void setMimeType(String value)
```


Establece el tipo MIME del archivo referenciado.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El tipo MIME del archivo referenciado. |

### setNamespaceMappings(String value) {#setNamespaceMappings-java.lang.String}
```
public void setNamespaceMappings(String value)
```


Establece los mapeos de espacios de nombres para consultas XPath.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | Las asignaciones de espacio de nombres para consultas XPath. |

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


Establece la ubicación del documento usando un IRI.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La ubicación del documento usando un IRI. |

### setTextConverter(String value) {#setTextConverter-java.lang.String}
```
public void setTextConverter(String value)
```


Establece el nombre del convertidor de texto para el formato del archivo incluido.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El nombre del convertidor de texto para el formato del archivo incluido. |

### setXPath(String value) {#setXPath-java.lang.String}
```
public void setXPath(String value)
```


Establece XPath para la porción deseada del archivo XML.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | XPath para la porción deseada del archivo XML. |

### setXslTransformation(String value) {#setXslTransformation-java.lang.String}
```
public void setXslTransformation(String value)
```


Establece la ubicación de la Transformación XSL para formatear datos XML.

 **Examples:** 

Muestra cómo crear un campo INCLUDETEXT y establecer sus propiedades.

```

 public void fieldIncludeText() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
     // 1 -  Perform an XSL transformation on an XML document:
     FieldIncludeText fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setXslTransformation(getMyDir() + "CD collection XSL transformation.xsl");

     builder.writeln();

     // 2 -  Use an XPath to take specific elements from an XML document:
     fieldIncludeText = createFieldIncludeText(builder, getMyDir() + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
     fieldIncludeText.setNamespaceMappings("xmlns:n='myNamespace'");
     fieldIncludeText.setXPath("/catalog/cd/title");

     doc.updateFields();
     doc.save(getArtifactsDir() + "Field.INCLUDETEXT.docx");
 }

 /// 
 /// Use a document builder to insert an INCLUDETEXT field with custom properties.
 /// 
 public FieldIncludeText createFieldIncludeText(DocumentBuilder builder, String sourceFullName, boolean lockFields, String mimeType, String textConverter, String encoding) throws Exception {
     FieldIncludeText fieldIncludeText = (FieldIncludeText) builder.insertField(FieldType.FIELD_INCLUDE_TEXT, true);
     fieldIncludeText.setSourceFullName(sourceFullName);
     fieldIncludeText.setLockFields(lockFields);
     fieldIncludeText.setMimeType(mimeType);
     fieldIncludeText.setTextConverter(textConverter);
     fieldIncludeText.setEncoding(encoding);

     return fieldIncludeText;
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | La ubicación de la Transformación XSL para formatear datos XML. |

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

