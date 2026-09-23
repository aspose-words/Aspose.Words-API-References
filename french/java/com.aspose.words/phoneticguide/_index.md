---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words pour Java"
description: "Représente le guide phonétique en Java."
type: docs
weight: 547
url: /fr/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Représente le Guide phonétique.
## Méthodes

| Méthode | Description |
| --- | --- |
| [getBaseText()](#getBaseText) | Obtient le texte de base du guide phonétique. |
| [getRubyText()](#getRubyText) | Obtient le texte ruby du guide phonétique. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Obtient le texte de base du guide phonétique.

 **Examples:** 

Montre comment obtenir les propriétés du guide phonétique.

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
java.lang.String - Texte de base du guide phonétique.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Obtient le texte ruby du guide phonétique.

 **Examples:** 

Montre comment obtenir les propriétés du guide phonétique.

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
java.lang.String - Texte ruby du guide phonétique.
