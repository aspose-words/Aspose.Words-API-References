---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words per Java"
description: "Rappresenta Phonetic Guide in Java."
type: docs
weight: 547
url: /it/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Rappresenta la Guida fonetica.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBaseText()](#getBaseText) | Ottiene il testo di base della guida fonetica. |
| [getRubyText()](#getRubyText) | Ottiene il testo ruby della guida fonetica. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Ottiene il testo di base della guida fonetica.

 **Examples:** 

Mostra come ottenere le proprietà della guida fonetica.

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
java.lang.String - Testo di base della guida fonetica.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Ottiene il testo ruby della guida fonetica.

 **Examples:** 

Mostra come ottenere le proprietà della guida fonetica.

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
java.lang.String - Testo ruby della guida fonetica.
