---
title: "مجموعة الإطارات"
linktitle: "مجموعة الإطارات"
second_title: "Aspose.Words لـ Java"
description: "يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات في جافا."
type: docs
weight: 353
url: /ar/java/com.aspose.words/frameset/
---

**Inheritance:**
java.lang.Object
```
public class Frameset
```

يمثل صفحة إطارات أو إطارًا واحدًا على صفحة إطارات.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

إذا كانت الخاصية [getChildFramesets()](../../com.aspose.words/frameset/\#getChildFramesets) تحتوي على عناصر، فإن هذه الحالة هي صفحة إطارات، وإلا فهي إطار واحد.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getChildFramesets()](#getChildFramesets) | يحصل على مجموعة الإطارات الفرعية وصفحات الإطارات. |
| [getFrameDefaultUrl()](#getFrameDefaultUrl) | يحصل على عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار. |
| [isFrameLinkToFile()](#isFrameLinkToFile) | يحصل على قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو موردًا خارجيًا يرتبط به الإطار. |
| [isFrameLinkToFile(boolean value)](#isFrameLinkToFile-boolean) | يضبط قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو موردًا خارجيًا يرتبط به الإطار. |
| [setFrameDefaultUrl(String value)](#setFrameDefaultUrl-java.lang.String) | يضبط عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار. |
### getChildFramesets() {#getChildFramesets}
```
public FramesetCollection getChildFramesets()
```


يحصل على مجموعة الإطارات الفرعية وصفحات الإطارات.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Returns:**
[FramesetCollection](../../com.aspose.words/framesetcollection/) - The collection of child frames and frames pages.
### getFrameDefaultUrl() {#getFrameDefaultUrl}
```
public String getFrameDefaultUrl()
```


يحصل على عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Returns:**
java.lang.String - عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار.
### isFrameLinkToFile() {#isFrameLinkToFile}
```
public boolean isFrameLinkToFile()
```


يحصل على قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو موردًا خارجيًا يرتبط به الإطار.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Returns:**
boolean - قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو مورد خارجي يرتبط به الإطار.
### isFrameLinkToFile(boolean value) {#isFrameLinkToFile-boolean}
```
public void isFrameLinkToFile(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو موردًا خارجيًا يرتبط به الإطار.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | قيمة تشير إلى ما إذا كان عنوان URL للصفحة ويب أو اسم ملف المستند المحدد في الخاصية [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) هو مورد خارجي يرتبط به الإطار. |

### setFrameDefaultUrl(String value) {#setFrameDefaultUrl-java.lang.String}
```
public void setFrameDefaultUrl(String value)
```


يضبط عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار.

 **Examples:** 

يعرض كيفية الوصول إلى الإطارات داخل الصفحة.

```

 // Document contains several frames with links to other documents.
 Document doc = new Document(getMyDir() + "Frameset.docx");

 Assert.assertEquals(3, doc.getFrameset().getChildFramesets().getCount());
 // We can check the default URL (a web page URL or local document) or if the frame is an external resource.
 Assert.assertEquals("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
         doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).getFrameDefaultUrl());
 Assert.assertTrue(doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile());

 Assert.assertEquals("Document.docx", doc.getFrameset().getChildFramesets().get(1).getFrameDefaultUrl());
 Assert.assertFalse(doc.getFrameset().getChildFramesets().get(1).isFrameLinkToFile());

 // Change properties for one of our frames.
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).setFrameDefaultUrl("https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx");
 doc.getFrameset().getChildFramesets().get(0).getChildFramesets().get(0).isFrameLinkToFile(false);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | عنوان URL للصفحة ويب أو اسم ملف المستند لعرضه في هذا الإطار. |

