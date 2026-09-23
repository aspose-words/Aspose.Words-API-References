---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words für Java"
description: "Stellt Phonetic Guide in Java dar."
type: docs
weight: 547
url: /de/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Stellt die phonetische Anleitung dar.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBaseText()](#getBaseText) | Liest den Basistext des phonetischen Leitfadens. |
| [getRubyText()](#getRubyText) | Liest den Ruby-Text des phonetischen Leitfadens. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Liest den Basistext des phonetischen Leitfadens.

 **Examples:** 

Zeigt, wie man die Eigenschaften des phonetischen Leitfadens abruft.

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
java.lang.String - Basistext des phonetischen Leitfadens.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Liest den Ruby-Text des phonetischen Leitfadens.

 **Examples:** 

Zeigt, wie man die Eigenschaften des phonetischen Leitfadens abruft.

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
java.lang.String - Ruby-Text des phonetischen Leitfadens.
