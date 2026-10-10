---
title: "SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Aspose.Words لـ Java"
description: "يتم إرجاع هذا الكائن إلى المستدعي بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها أثناء عملية الحفظ في جافا."
type: docs
weight: 597
url: /ar/java/com.aspose.words/saveoutputparameters/
---

**Inheritance:**
java.lang.Object
```
public class SaveOutputParameters
```

يتم إرجاع هذا الكائن إلى المستدعي بعد حفظ المستند ويحتوي على معلومات إضافية تم إنشاؤها أو حسابها أثناء عملية الحفظ. يمكن للمستدعي استخدام هذا الكائن أو تجاهله.

للتعرف على المزيد، زر [ Save a Document ][Save a Document] مقالة الوثائق.

 **Examples:** 

يعرض كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getContentType()](#getContentType) | يرجع سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ. |
### getContentType() {#getContentType}
```
public String getContentType()
```


يرجع سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ.

 **Examples:** 

يعرض كيفية الوصول إلى معلمات الإخراج لعملية حفظ المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // After we save a document, we can access the Internet Media Type (MIME type) of the newly created output document.
 SaveOutputParameters parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.doc");

 Assert.assertEquals("application/msword", parameters.getContentType());

 // This property changes depending on the save format.
 parameters = doc.save(getArtifactsDir() + "Document.SaveOutputParameters.pdf");

 Assert.assertEquals("application/pdf", parameters.getContentType());
 
```

**Returns:**
java.lang.String - سلسلة Content-Type (نوع وسائط الإنترنت) التي تحدد نوع المستند المحفوظ.
