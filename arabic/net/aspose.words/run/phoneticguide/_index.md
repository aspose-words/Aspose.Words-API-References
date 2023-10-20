---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words لـ .NET
description: Run PhoneticGuide ملكية. يحصل علىPhoneticGuide الكائن في C#.
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
