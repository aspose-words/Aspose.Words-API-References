---
title: PhoneticGuide.BaseText
second_title: Aspose.Words لمراجع .NET API
description: PhoneticGuide ملكية. يحصل على النص الأساسي للدليل الصوتي.
type: docs
weight: 10
url: /ar/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

يحصل على النص الأساسي للدليل الصوتي.

```csharp
public string BaseText { get; }
```

### أمثلة

يبين كيفية الحصول على خصائص الدليل الصوتي.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// استخدم الدليل الصوتي في النص الآسيوي.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### أنظر أيضا

* class [PhoneticGuide](../)
* مساحة الاسم [Aspose.Words](../../phoneticguide/)
* المجسم [Aspose.Words](../../../)


