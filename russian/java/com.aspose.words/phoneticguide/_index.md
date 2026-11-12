---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words для Java"
description: "Представляет Phonetic Guide в Java."
type: docs
weight: 547
url: /ru/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

Представляет фонетический справочник.
## Методы

| Метод | Описание |
| --- | --- |
| [getBaseText()](#getBaseText) | Получает базовый текст фонетического руководства. |
| [getRubyText()](#getRubyText) | Получает ruby‑текст фонетического руководства. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


Получает базовый текст фонетического руководства.

 **Examples:** 

Показывает, как получить свойства фонетической подсказки.

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
java.lang.String — базовый текст фонетического руководства.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


Получает ruby‑текст фонетического руководства.

 **Examples:** 

Показывает, как получить свойства фонетической подсказки.

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
java.lang.String — ruby‑текст фонетического руководства.
