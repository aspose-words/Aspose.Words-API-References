---
title: "Frameset"
linktitle: "Frameset"
second_title: "Aspose.Words pour Java"
description: "Représente une page de cadres ou un seul cadre sur une page de cadres en Java."
type: docs
weight: 353
url: /fr/java/com.aspose.words/frameset/
---

**Inheritance:**
java.lang.Object
```
public class Frameset
```

Représente une page de cadres ou un cadre unique sur une page de cadres.

Pour en savoir plus, consultez l'article de documentation [ Programming with Documents ][Programming with Documents].

 **Remarks:** 

Si la propriété [getChildFramesets()](../../com.aspose.words/frameset/\#getChildFramesets) contient des éléments, cette instance est une page de cadres, sinon c’est un seul cadre.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getChildFramesets()](#getChildFramesets) | Obtient la collection des cadres enfants et des pages de cadres. |
| [getFrameDefaultUrl()](#getFrameDefaultUrl) | Obtient l'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre. |
| [isFrameLinkToFile()](#isFrameLinkToFile) | Obtient une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié. |
| [isFrameLinkToFile(boolean value)](#isFrameLinkToFile-boolean) | Définit une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié. |
| [setFrameDefaultUrl(String value)](#setFrameDefaultUrl-java.lang.String) | Définit l'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre. |
### getChildFramesets() {#getChildFramesets}
```
public FramesetCollection getChildFramesets()
```


Obtient la collection des cadres enfants et des pages de cadres.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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


Obtient l'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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
java.lang.String - L'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre.
### isFrameLinkToFile() {#isFrameLinkToFile}
```
public boolean isFrameLinkToFile()
```


Obtient une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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
boolean - Une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié.
### isFrameLinkToFile(boolean value) {#isFrameLinkToFile-boolean}
```
public void isFrameLinkToFile(boolean value)
```


Définit une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | boolean | Une valeur indiquant si la page Web ou le nom de fichier du document spécifié dans la propriété [getFrameDefaultUrl()](../../com.aspose.words/frameset/\#getFrameDefaultUrl) / [setFrameDefaultUrl(java.lang.String)](../../com.aspose.words/frameset/\#setFrameDefaultUrl-java.lang.String) est une ressource externe à laquelle le cadre est lié. |

### setFrameDefaultUrl(String value) {#setFrameDefaultUrl-java.lang.String}
```
public void setFrameDefaultUrl(String value)
```


Définit l'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre.

 **Examples:** 

Montre comment accéder aux cadres sur la page.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | L'URL de la page Web ou le nom de fichier du document à afficher dans ce cadre. |

