---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words para Java"
description: "Representa la Guía Fonética en Java."
type: docs
weight: 547
url: /es/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Representa la Guía Fonética.
## Métodos

| Método | Descripción |
| --- | --- |
| [getBaseText()](#getBaseText) | Obtiene el texto base de la guía fonética. |
| [getRubyText()](#getRubyText) | Obtiene el texto ruby de la guía fonética. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Obtiene el texto base de la guía fonética.

 **Examples:** 

Muestra cómo obtener las propiedades de la guía fonética.

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
java.lang.String - Texto base de la guía fonética.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Obtiene el texto ruby de la guía fonética.

 **Examples:** 

Muestra cómo obtener las propiedades de la guía fonética.

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
java.lang.String - Texto ruby de la guía fonética.
