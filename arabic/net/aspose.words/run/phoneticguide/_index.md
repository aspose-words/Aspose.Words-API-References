---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words لـ .NET
description: حسّن مهاراتك اللغوية وتواصلك مع PhoneticGuide. حسّن مهاراتك اللغوية وتواصلك من خلال الوصول إلى رؤى صوتية مخصصة.
type: docs
weight: 40
url: /ar/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

يحصل على`PhoneticGuide` الكائن.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
