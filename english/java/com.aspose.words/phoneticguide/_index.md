---
title: PhoneticGuide
linktitle: PhoneticGuide
second_title: Aspose.Words for Java
description: Represents Phonetic Guide in Java.
type: docs
weight: 500
url: /java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Represents Phonetic Guide.
## Methods

| Method | Description |
| --- | --- |
| [getBaseText()](#getBaseText) | Gets base text of the phonetic guide. |
| [getRubyText()](#getRubyText) | Gets ruby text of the phonetic guide. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Gets base text of the phonetic guide.

 **Examples:** 

Shows how to get properties of the phonetic guide.

```

 Document doc = new Document(getMyDir() + "Phonetic guide.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 // Use phonetic guide in the Asian text.
 Assert.assertEquals(true, runs.get(0).isPhoneticGuide());
 Assert.assertEquals("base", runs.get(0).getPhoneticGuide().getBaseText());
 Assert.assertEquals("ruby", runs.get(0).getPhoneticGuide().getRubyText());
 
```

**Returns:**
java.lang.String - Base text of the phonetic guide.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Gets ruby text of the phonetic guide.

 **Examples:** 

Shows how to get properties of the phonetic guide.

```

 Document doc = new Document(getMyDir() + "Phonetic guide.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();

 // Use phonetic guide in the Asian text.
 Assert.assertEquals(true, runs.get(0).isPhoneticGuide());
 Assert.assertEquals("base", runs.get(0).getPhoneticGuide().getBaseText());
 Assert.assertEquals("ruby", runs.get(0).getPhoneticGuide().getRubyText());
 
```

**Returns:**
java.lang.String - Ruby text of the phonetic guide.
