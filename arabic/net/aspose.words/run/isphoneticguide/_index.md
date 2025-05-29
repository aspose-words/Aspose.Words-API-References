---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words لـ .NET
description: اكتشف IsPhoneticGuide، وهي أداة قوية تحدد ما إذا كان التشغيل بمثابة دليل صوتي، مما يعزز وضوح النص وقابليته للقراءة.
type: docs
weight: 20
url: /ar/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

يحصل على قيمة منطقية تشير إلى أن التشغيل عبارة عن دليل صوتي.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
