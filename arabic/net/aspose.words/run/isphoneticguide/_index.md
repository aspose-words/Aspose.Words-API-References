---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words لـ .NET
description: Run IsPhoneticGuide ملكية. الحصول على قيمة منطقية تشير إلى أن التشغيل هو دليل صوتي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

الحصول على قيمة منطقية تشير إلى أن التشغيل هو دليل صوتي.

```csharp
public bool IsPhoneticGuide { get; }
```

## أمثلة

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

* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
