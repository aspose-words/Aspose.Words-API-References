---
title: PhoneticGuide
linktitle: PhoneticGuide
second_title: Aspose.Words for Java
description: Represents Phonetic Guide in Java.
type: docs
weight: 521
url: /java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Represents Phonetic Guide.

 **Examples:** 

Shows how to get properties of the phonetic guide.

```

 Document doc = new Document(getMyDir() + "Phonetic guide.docx");

 RunCollection runs = doc.getFirstSection().getBody().getFirstParagraph().getRuns();
 // Use phonetic guide in the Asian text.
 Assert.assertEquals(true, runs.get(0).isPhoneticGuide());

 PhoneticGuide phoneticGuide = runs.get(0).getPhoneticGuide();
 Assert.assertEquals("base", phoneticGuide.getBaseText());
 Assert.assertEquals("ruby", phoneticGuide.getRubyText());
 
```
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

 PhoneticGuide phoneticGuide = runs.get(0).getPhoneticGuide();
 Assert.assertEquals("base", phoneticGuide.getBaseText());
 Assert.assertEquals("ruby", phoneticGuide.getRubyText());
 
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

 PhoneticGuide phoneticGuide = runs.get(0).getPhoneticGuide();
 Assert.assertEquals("base", phoneticGuide.getBaseText());
 Assert.assertEquals("ruby", phoneticGuide.getRubyText());
 
```

**Returns:**
java.lang.String - Ruby text of the phonetic guide.
