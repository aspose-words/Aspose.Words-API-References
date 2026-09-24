---
title: "Frameset"
linktitle: "Frameset"
second_title: "Aspose.Words Java için"
description: "Java'da bir çerçeve sayfasını veya çerçeve sayfasındaki tek bir çerçeveyi temsil eder."
type: docs
weight: 353
url: /tr/java/com.aspose.words/frameset/
---

**Inheritance:**
java.lang.Object
```
public class Frameset
```

Çerçeve sayfasını veya bir çerçeve sayfasındaki tek bir çerçeveyi temsil eder.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Eğer [getChildFramesets()](../../com.aspose.words/frameset/\#getChildFramesets) özelliği öğeler içeriyorsa, bu örnek bir çerçeve sayfasıdır; aksi takdirde tek bir çerçevedir.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getChildFramesets()](#getChildFramesets) | Alt çerçevelerin ve çerçeve sayfalarının koleksiyonunu alır. |
| [getFrameDefaultUrl()](#getFrameDefaultUrl) | Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını alır. |
| [isFrameLinkToFile()](#isFrameLinkToFile) | Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değeri, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için alır. |
| [isFrameLinkToFile(boolean value)](#isFrameLinkToFile-boolean) | Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değeri, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için ayarlar. |
| [setFrameDefaultUrl(String value)](#setFrameDefaultUrl-java.lang.String) | Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını ayarlar. |
### getChildFramesets() {#getChildFramesets}
```
public FramesetCollection getChildFramesets()
```


Alt çerçevelerin ve çerçeve sayfalarının koleksiyonunu alır.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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


Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını alır.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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
java.lang.String - Bu çerçevede görüntülenecek web sayfası URL'si veya belge dosya adı.
### isFrameLinkToFile() {#isFrameLinkToFile}
```
public boolean isFrameLinkToFile()
```


Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değeri, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için alır.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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
boolean - Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değer, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için.
### isFrameLinkToFile(boolean value) {#isFrameLinkToFile-boolean}
```
public void isFrameLinkToFile(boolean value)
```


Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değeri, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için ayarlar.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | Bu çerçevenin bağlı olduğu harici bir kaynak olup olmadığını belirten değer, [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) özelliğinde belirtilen web sayfası veya belge dosya adı için. |

### setFrameDefaultUrl(String value) {#setFrameDefaultUrl-java.lang.String}
```
public void setFrameDefaultUrl(String value)
```


Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını ayarlar.

 **Examples:** 

Sayfa üzerindeki çerçevelere nasıl erişileceğini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Bu çerçevede görüntülenecek web sayfası URL'si veya belge dosya adı. |

