---
title: "FieldDde"
linktitle: "FieldDde"
second_title: "Aspose.Words Java için"
description: "Java'da DDE alanını uygular."
type: docs
weight: 221
url: /tr/java/com.aspose.words/fielddde/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldDde extends Field
```

DDE alanını uygular.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Başka bir uygulamadan kopyalanan bilgi için, bu alan DDE kullanarak bilgiyi orijinal kaynak dosyasına bağlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAutoUpdate()](#getAutoUpdate) | Bu alanın otomatik olarak güncellenip güncellenmeyeceğini alır. |
| [getDisplayResult()](#getDisplayResult) | Görüntülenen alan sonucunu temsil eden metni alır. |
| [getEnd()](#getEnd) | Alan sonunu temsil eden düğümü alır. |
| [getFieldCode()](#getFieldCode) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFormat()](#getFormat) | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır. |
| [getInsertAsBitmap()](#getInsertAsBitmap) | Bağlı nesnenin bitmap olarak eklenip eklenmeyeceğini alır. |
| [getInsertAsHtml()](#getInsertAsHtml) | Bağlı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini alır. |
| [getInsertAsPicture()](#getInsertAsPicture) | Bağlı nesnenin resim olarak eklenip eklenmeyeceğini alır. |
| [getInsertAsRtf()](#getInsertAsRtf) | Bağlı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini alır. |
| [getInsertAsText()](#getInsertAsText) | Bağlı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini alır. |
| [getInsertAsUnicode()](#getInsertAsUnicode) | Bağlı nesnenin Unicode metin olarak eklenip eklenmeyeceğini alır. |
| [getLocaleId()](#getLocaleId) | Alanının LCID'sini alır. |
| [getProgId()](#getProgId) | Bağlantı bilgilerinin uygulama türünü alır. |
| [getResult()](#getResult) | Alan ayırıcı ile alan sonu arasındaki metni alır. |
| [getSeparator()](#getSeparator) | Alan ayırıcıyı temsil eden düğümü alır. |
| [getSourceFullName()](#getSourceFullName) | Kaynak dosyanın adını ve konumunu alır. |
| [getSourceItem()](#getSourceItem) | Bağlantı verilen kaynak dosyanın bölümünü alır. |
| [getStart()](#getStart) | Alan başlangıcını temsil eden düğümü alır. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Microsoft Word alan türünü alır. |
| [isDirty()](#isDirty) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır. |
| [isDirty(boolean value)](#isDirty-boolean) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar. |
| [isLinked()](#isLinked) | Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceğini alır. |
| [isLinked(boolean value)](#isLinked-boolean) | Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceğini ayarlar. |
| [isLocked()](#isLocked) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır. |
| [isLocked(boolean value)](#isLocked-boolean) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar. |
| [remove()](#remove) | Alanı belgeden kaldırır. |
| [setAutoUpdate(boolean value)](#setAutoUpdate-boolean) | Bu alanın otomatik olarak güncellenip güncellenmeyeceğini ayarlar. |
| [setInsertAsBitmap(boolean value)](#setInsertAsBitmap-boolean) | Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceğini ayarlar. |
| [setInsertAsHtml(boolean value)](#setInsertAsHtml-boolean) | Bağlantılı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini ayarlar. |
| [setInsertAsPicture(boolean value)](#setInsertAsPicture-boolean) | Bağlantılı nesnenin resim olarak eklenip eklenmeyeceğini ayarlar. |
| [setInsertAsRtf(boolean value)](#setInsertAsRtf-boolean) | Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini ayarlar. |
| [setInsertAsText(boolean value)](#setInsertAsText-boolean) | Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini ayarlar. |
| [setInsertAsUnicode(boolean value)](#setInsertAsUnicode-boolean) | Bağlantılı nesnenin Unicode metin olarak eklenip eklenmeyeceğini ayarlar. |
| [setLocaleId(int value)](#setLocaleId-int) | Alanının LCID'sini ayarlar. |
| [setProgId(String value)](#setProgId-java.lang.String) | Bağlantı bilgilerinin uygulama türünü ayarlar. |
| [setResult(String value)](#setResult-java.lang.String) | Alan ayırıcı ile alan sonu arasındaki metni ayarlar. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String) | Kaynak dosyanın adını ve konumunu ayarlar. |
| [setSourceItem(String value)](#setSourceItem-java.lang.String) | Bağlantı verilen kaynak dosyanın bölümünü ayarlar. |
| [unlink()](#unlink) | Alan bağlantısını kaldırır. |
| [update()](#update) | Alan güncellemesini gerçekleştirir. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Bir alan güncellemesi gerçekleştirir. |
### getAutoUpdate() {#getAutoUpdate}
```
public boolean getAutoUpdate()
```


Bu alanın otomatik olarak güncellenip güncellenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bu alanın otomatik olarak güncellenip güncellenmeyeceği.
### getDisplayResult() {#getDisplayResult}
```
public String getDisplayResult()
```


Görüntülenen alan sonucunu temsil eden metni alır.

 **Remarks:** 

Doğru değer elde etmek için [Document.updateListLabels()](../../com.aspose.words/document/\#updateListLabels) yöntemi, [FieldListNum](../../com.aspose.words/fieldlistnum/), [FieldAutoNum](../../com.aspose.words/fieldautonum/), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout/) ve [FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl/) alanları için çağrılmalıdır.

 **Examples:** 

Bir alanın belgede gösterdiği gerçek metni nasıl alacağınızı gösterir.

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
java.lang.String - Görüntülenen alan sonucunu temsil eden metin.
### getEnd() {#getEnd}
```
public FieldEnd getEnd()
```


Alan sonunu temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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


Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların sonuçları dahil edilir.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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


Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür.

 **Examples:** 

Bir alanın alan kodunu nasıl alacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| includeChildFieldCodes | boolean | true  eğer alt alan kodları dahil edilmeliyse. |

**Returns:**
java.lang.String
### getFormat() {#getFormat}
```
public FieldFormat getFormat()
```


Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır.

 **Examples:** 

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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


Bağlı nesnenin bitmap olarak eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceği.
### getInsertAsHtml() {#getInsertAsHtml}
```
public boolean getInsertAsHtml()
```


Bağlı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceği.
### getInsertAsPicture() {#getInsertAsPicture}
```
public boolean getInsertAsPicture()
```


Bağlı nesnenin resim olarak eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin resim olarak eklenip eklenmeyeceği.
### getInsertAsRtf() {#getInsertAsRtf}
```
public boolean getInsertAsRtf()
```


Bağlı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceği.
### getInsertAsText() {#getInsertAsText}
```
public boolean getInsertAsText()
```


Bağlı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceği.
### getInsertAsUnicode() {#getInsertAsUnicode}
```
public boolean getInsertAsUnicode()
```


Bağlı nesnenin Unicode metin olarak eklenip eklenmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Bağlantılı nesnenin Unicode metin olarak eklenip eklenmeyeceği.
### getLocaleId() {#getLocaleId}
```
public int getLocaleId()
```


Alanının LCID'sini alır.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
int - Alanın LCID'si.
### getProgId() {#getProgId}
```
public String getProgId()
```


Bağlantı bilgilerinin uygulama türünü alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
java.lang.String - Bağlantı bilgilerinin uygulama türü.
### getResult() {#getResult}
```
public String getResult()
```


Alan ayırıcı ile alan sonu arasındaki metni alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
java.lang.String - Alan ayırıcı ile alan sonu arasındaki metin.
### getSeparator() {#getSeparator}
```
public FieldSeparator getSeparator()
```


Alan ayırıcıyı temsil eden düğümü alır. Null olabilir.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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


Kaynak dosyanın adını ve konumunu alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
java.lang.String - Kaynak dosyanın adı ve konumu.
### getSourceItem() {#getSourceItem}
```
public String getSourceItem()
```


Bağlantı verilen kaynak dosyanın bölümünü alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
java.lang.String - Bağlantı verilen kaynak dosyanın bölümü.
### getStart() {#getStart}
```
public FieldStart getStart()
```


Alan başlangıcını temsil eden düğümü alır.

 **Examples:** 

Alan koleksiyonu ile nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Returns:**
int
### getType() {#getType}
```
public int getType()
```


Microsoft Word alan türünü alır.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Returns:**
int - Microsoft Word alan türü. Döndürülen değer, [FieldType](../../com.aspose.words/fieldtype/) sabitlerinden biridir.
### isDirty() {#isDirty}
```
public boolean isDirty()
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
boolean - Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı.
### isDirty(boolean value) {#isDirty-boolean}
```
public void isDirty(boolean value)
```


Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar.

 **Examples:** 

Alan sonucunu güncellemek için özel özelliğin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın mevcut sonucunun, belgeye yapılan diğer değişiklikler nedeniyle artık doğru olmaması (eski) olup olmadığı. |

### isLinked() {#isLinked}
```
public boolean isLinked()
```


Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceğini alır.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
boolean - Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceği.
### isLinked(boolean value) {#isLinked-boolean}
```
public void isLinked(boolean value)
```


Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Grafik verileri belgeyle birlikte saklanmayarak dosya boyutunun küçültülüp küçültülmeyeceği. |

### isLocked() {#isLocked}
```
public boolean isLocked()
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
boolean - Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı).
### isLocked(boolean value) {#isLocked-boolean}
```
public void isLocked(boolean value)
```


Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar.

 **Examples:** 

Bir FieldStart düğümüyle nasıl çalışılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Alanın kilitli olup olmadığı (sonucunu yeniden hesaplamamalı). |

### remove() {#remove}
```
public Node remove()
```


Alanı belgeden kaldırır. Alanın hemen sonrasında bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğuysa, üst paragrafı döndürür. Alan zaten kaldırılmışsa, null döndürür.

 **Examples:** 

Bir alan koleksiyonundan alanların nasıl kaldırılacağını gösterir.

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

PRIVATE alanların nasıl işleneceğini gösterir.

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


Bu alanın otomatik olarak güncellenip güncellenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bu alanın otomatik olarak güncellenip güncellenmeyeceği. |

### setInsertAsBitmap(boolean value) {#setInsertAsBitmap-boolean}
```
public void setInsertAsBitmap(boolean value)
```


Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin bitmap olarak eklenip eklenmeyeceği. |

### setInsertAsHtml(boolean value) {#setInsertAsHtml-boolean}
```
public void setInsertAsHtml(boolean value)
```


Bağlantılı nesnenin HTML biçiminde metin olarak eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin HTML formatında metin olarak eklenip eklenmeyeceği. |

### setInsertAsPicture(boolean value) {#setInsertAsPicture-boolean}
```
public void setInsertAsPicture(boolean value)
```


Bağlantılı nesnenin resim olarak eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin resim olarak eklenip eklenmeyeceği. |

### setInsertAsRtf(boolean value) {#setInsertAsRtf-boolean}
```
public void setInsertAsRtf(boolean value)
```


Bağlantılı nesnenin zengin metin biçiminde (RTF) eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin zengin metin formatında (RTF) eklenip eklenmeyeceği. |

### setInsertAsText(boolean value) {#setInsertAsText-boolean}
```
public void setInsertAsText(boolean value)
```


Bağlantılı nesnenin yalnızca metin biçiminde eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin yalnızca metin formatında eklenip eklenmeyeceği. |

### setInsertAsUnicode(boolean value) {#setInsertAsUnicode-boolean}
```
public void setInsertAsUnicode(boolean value)
```


Bağlantılı nesnenin Unicode metin olarak eklenip eklenmeyeceğini ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Bağlantılı nesnenin Unicode metin olarak eklenip eklenmeyeceği. |

### setLocaleId(int value) {#setLocaleId-int}
```
public void setLocaleId(int value)
```


Alanının LCID'sini ayarlar.

 **Examples:** 

Bir alanı nasıl ekleyeceğinizi ve yerel ayarıyla nasıl çalışacağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Alanın LCID'si. |

### setProgId(String value) {#setProgId-java.lang.String}
```
public void setProgId(String value)
```


Bağlantı bilgilerinin uygulama türünü ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bağlantı bilgilerinin uygulama türü. |

### setResult(String value) {#setResult-java.lang.String}
```
public void setResult(String value)
```


Alan ayırıcı ile alan sonu arasındaki metni ayarlar.

 **Examples:** 

Alan kodu kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Field dateField = builder.insertField("DATE \\* MERGEFORMAT");

 Assert.assertEquals(FieldType.FIELD_DATE, dateField.getType());
 Assert.assertEquals("DATE \\* MERGEFORMAT", dateField.getFieldCode());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Alan ayırıcı ile alan sonu arasındaki metin. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String}
```
public void setSourceFullName(String value)
```


Kaynak dosyanın adını ve konumunu ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Kaynak dosyanın adı ve konumu. |

### setSourceItem(String value) {#setSourceItem-java.lang.String}
```
public void setSourceItem(String value)
```


Bağlantı verilen kaynak dosyanın bölümünü ayarlar.

 **Examples:** 

Yerel dosya sistemindeki diğer belgelere bağlanmak ve içeriklerini göstermek için çeşitli alan türlerinin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bağlantı verilen kaynak dosyanın bölümü. |

### unlink() {#unlink}
```
public boolean unlink()
```


Alan bağlantısını kaldırır.

 **Remarks:** 

Alanı en son sonucu ile değiştirir.

XE (Dizin Girişi) alanları ve SEQ (Sıra) alanları gibi bazı alanlar bağlantısı kesilemez.

 **Examples:** 

Bir alanın bağlantısını nasıl keseceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Linked fields.docx");
 doc.getRange().getFields().get(1).unlink();
 
```

**Returns:**
boolean -  true  ise alanın bağlantısı kesilmiş demektir, aksi takdirde  false .
### update() {#update}
```
public void update()
```


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

FieldType kullanarak bir alanı belgeye nasıl ekleyeceğinizi gösterir.

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

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

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


Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa bir istisna fırlatır.

 **Examples:** 

Bir belge yüklenirken INCLUDEPICTURE alanlarını korumanın veya atmanın nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| ignoreMergeFormat | boolean | true ise, MERGEFORMAT anahtarına bakılmaksızın doğrudan alan sonucu biçimlendirmesi bırakılır, aksi takdirde normal güncelleme yapılır. |

