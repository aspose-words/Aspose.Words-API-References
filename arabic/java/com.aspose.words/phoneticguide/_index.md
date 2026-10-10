---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words لـ Java"
description: "يمثل دليل النطق في جافا."
type: docs
weight: 547
url: /ar/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

يمثل الدليل الصوتي.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBaseText()](#getBaseText) | يحصل على النص الأساسي لدليل النطق. |
| [getRubyText()](#getRubyText) | يحصل على نص الروبي لدليل النطق. |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


يحصل على النص الأساسي لدليل النطق.

 **Examples:** 

يوضح كيفية الحصول على خصائص الدليل الصوتي.

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
java.lang.String - النص الأساسي لدليل النطق.
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


يحصل على نص الروبي لدليل النطق.

 **Examples:** 

يوضح كيفية الحصول على خصائص الدليل الصوتي.

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
java.lang.String - نص الروبي لدليل النطق.
