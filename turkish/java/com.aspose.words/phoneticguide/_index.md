---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words Java için"
description: "Java'da Fonetik Kılavuzu temsil eder."
type: docs
weight: 547
url: /tr/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Fonetik Kılavuzu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBaseText()](#getBaseText) | Fonetik kılavuzun temel metnini alır. |
| [getRubyText()](#getRubyText) | Fonetik kılavuzun ruby metnini alır. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Fonetik kılavuzun temel metnini alır.

 **Examples:** 

Fonetik kılavuzun özelliklerini nasıl alacağınızı gösterir.

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
java.lang.String - Fonetik kılavuzun temel metni.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Fonetik kılavuzun ruby metnini alır.

 **Examples:** 

Fonetik kılavuzun özelliklerini nasıl alacağınızı gösterir.

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
java.lang.String - Fonetik kılavuzun ruby metni.
