---
title: "PhoneticGuide"
linktitle: "PhoneticGuide"
second_title: "Aspose.Words for Java"
description: "表示 Java 中的拼音指南。"
type: docs
weight: 547
url: /zh/java/com.aspose.words/phoneticguide/
---

**Inheritance:**
java.lang.Object
```
public class PhoneticGuide
```

表示音标指南。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getBaseText()](#getBaseText) | 获取音标指南的基础文本。 |
| [getRubyText()](#getRubyText) | 获取音标指南的 ruby 文本。 |
### getBaseText() {#getBaseText}
```
public String getBaseText()
```


获取音标指南的基础文本。

 **Examples:** 

展示如何获取音标指南的属性。

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
java.lang.String - 音标指南的基础文本。
### getRubyText() {#getRubyText}
```
public String getRubyText()
```


获取音标指南的 ruby 文本。

 **Examples:** 

展示如何获取音标指南的属性。

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
java.lang.String - 音标指南的 ruby 文本。
