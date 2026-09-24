---
title: "FieldSaveDate"
linktitle: "FieldSaveDate"
second_title: "Aspose.Words Java için"
description: "Java'da SAVEDATE alanını uygular."
type: docs
weight: 280
url: /tr/java/com.aspose.words/fieldsavedate/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field/)
```
public class FieldSaveDate extends Field
```

SAVEDATE alanını uygular.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Belgenin en son kaydedildiği tarih ve zamanı alır. Varsayılan olarak, Gregoryen takvim kullanılır.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getDisplayResult()](#getDisplayResult) | Görüntülenen alan sonucunu temsil eden metni alır. |
| [getEnd()](#getEnd) | Alan sonunu temsil eden düğümü alır. |
| [getFieldCode()](#getFieldCode) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean) | Alan başlangıcı ile alan ayırıcı arasındaki metni (veya ayırıcı yoksa alan sonunu) döndürür. |
| [getFormat()](#getFormat) | Alan biçimlendirmesine tipli erişim sağlayan bir [FieldFormat](../../com.aspose.words/fieldformat/) nesnesi alır. |
| [getLocaleId()](#getLocaleId) | Alanının LCID'sini alır. |
| [getResult()](#getResult) | Alan ayırıcı ile alan sonu arasındaki metni alır. |
| [getSeparator()](#getSeparator) | Alan ayırıcıyı temsil eden düğümü alır. |
| [getStart()](#getStart) | Alan başlangıcını temsil eden düğümü alır. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String) |  |
| [getType()](#getType) | Microsoft Word alan türünü alır. |
| [getUseLunarCalendar()](#getUseLunarCalendar) | Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağını alır. |
| [getUseSakaEraCalendar()](#getUseSakaEraCalendar) | Saka Çağı takviminin kullanılıp kullanılmayacağını alır. |
| [getUseUmAlQuraCalendar()](#getUseUmAlQuraCalendar) | Um-al-Qura takviminin kullanılıp kullanılmayacağını alır. |
| [isDirty()](#isDirty) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını alır. |
| [isDirty(boolean value)](#isDirty-boolean) | Belgenin diğer değişiklikleri nedeniyle alanın mevcut sonucunun artık doğru (eski) olup olmadığını ayarlar. |
| [isLocked()](#isLocked) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) alır. |
| [isLocked(boolean value)](#isLocked-boolean) | Alan kilitli olup olmadığını (sonucunu yeniden hesaplamamalı) ayarlar. |
| [remove()](#remove) | Alanı belgeden kaldırır. |
| [setLocaleId(int value)](#setLocaleId-int) | Alanının LCID'sini ayarlar. |
| [setResult(String value)](#setResult-java.lang.String) | Alan ayırıcı ile alan sonu arasındaki metni ayarlar. |
| [setUseLunarCalendar(boolean value)](#setUseLunarCalendar-boolean) | Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağını ayarlar. |
| [setUseSakaEraCalendar(boolean value)](#setUseSakaEraCalendar-boolean) | Saka Çağı takviminin kullanılıp kullanılmayacağını ayarlar. |
| [setUseUmAlQuraCalendar(boolean value)](#setUseUmAlQuraCalendar-boolean) | Um-al-Qura takviminin kullanılıp kullanılmayacağını ayarlar. |
| [unlink()](#unlink) | Alan bağlantısını kaldırır. |
| [update()](#update) | Alan güncellemesini gerçekleştirir. |
| [update(boolean ignoreMergeFormat)](#update-boolean) | Bir alan güncellemesi gerçekleştirir. |
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
### getUseLunarCalendar() {#getUseLunarCalendar}
```
public boolean getUseLunarCalendar()
```


Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağını alır.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Returns:**
boolean - Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağı.
### getUseSakaEraCalendar() {#getUseSakaEraCalendar}
```
public boolean getUseSakaEraCalendar()
```


Saka Çağı takviminin kullanılıp kullanılmayacağını alır.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Returns:**
boolean - Saka Çağı takviminin kullanılıp kullanılmayacağı.
### getUseUmAlQuraCalendar() {#getUseUmAlQuraCalendar}
```
public boolean getUseUmAlQuraCalendar()
```


Um-al-Qura takviminin kullanılıp kullanılmayacağını alır.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Returns:**
boolean - Um-al-Qura takviminin kullanılıp kullanılmayacağı.
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

### setUseLunarCalendar(boolean value) {#setUseLunarCalendar-boolean}
```
public void setUseLunarCalendar(boolean value)
```


Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağını ayarlar.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Hicri Ay takvimi mi yoksa İbrani Ay takvimi mi kullanılacağı. |

### setUseSakaEraCalendar(boolean value) {#setUseSakaEraCalendar-boolean}
```
public void setUseSakaEraCalendar(boolean value)
```


Saka Çağı takviminin kullanılıp kullanılmayacağını ayarlar.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Saka Dönemi takvimini kullanıp kullanmayacağını. |

### setUseUmAlQuraCalendar(boolean value) {#setUseUmAlQuraCalendar-boolean}
```
public void setUseUmAlQuraCalendar(boolean value)
```


Um-al-Qura takviminin kullanılıp kullanılmayacağını ayarlar.

 **Examples:** 

Microsoft Word kullanılarak gerçekleştirilen belgenin en son kaydetme işleminin tarih/saatini göstermek için SAVEDATE alanının nasıl kullanılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Document.docx");
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.writeln(" Date this document was last saved:");

 // We can use the SAVEDATE field to display the last save operation's date and time on the document.
 // The save operation that these fields refer to is the manual save in an application like Microsoft Word,
 // not the document's Save method.
 // Below are three different calendar types according to which the SAVEDATE field can display the date/time.
 // 1 -  Islamic Lunar Calendar:
 builder.write("According to the Lunar Calendar - ");
 FieldSaveDate field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseLunarCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\h", field.getFieldCode());

 // 2 -  Umm al-Qura calendar:
 builder.write("\nAccording to the Umm al-Qura calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseUmAlQuraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\u", field.getFieldCode());

 // 3 -  Indian National calendar:
 builder.write("\nAccording to the Indian National calendar - ");
 field = (FieldSaveDate) builder.insertField(FieldType.FIELD_SAVE_DATE, true);
 field.setUseSakaEraCalendar(true);

 Assert.assertEquals(" SAVEDATE  \\s", field.getFieldCode());

 // The SAVEDATE fields draw their date/time values from the LastSavedTime built-in property.
 // The document's Save method will not update this value, but we can still update it manually.
 doc.getBuiltInDocumentProperties().setLastSavedTime(new Date());

 doc.updateFields();
 doc.save(getArtifactsDir() + "Field.SAVEDATE.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Um-al-Qura takvimini kullanıp kullanmayacağını. |

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

