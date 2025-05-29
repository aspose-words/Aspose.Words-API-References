---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PhoneticGuide BaseText للوصول بسهولة إلى نص الدليل الصوتي الأساسي وتحسينه لتحسين الوضوح والتواصل.
type: docs
weight: 10
url: /ar/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

يحصل على النص الأساسي للدليل الصوتي.

```csharp
public string BaseText { get; }
```

## أمثلة

يوضح كيفية الحصول على خصائص الدليل الصوتي.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// استخدم الدليل الصوتي في النص الآسيوي.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### أنظر أيضا

* class [PhoneticGuide](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
