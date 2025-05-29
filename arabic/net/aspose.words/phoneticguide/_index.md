---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.PhoneticGuide لتحسين سهولة قراءة النصوص باستخدام الأدلة الصوتية. حسّن تجربة المستخدم وإمكانية الوصول بسهولة!
type: docs
weight: 5160
url: /ar/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

يمثل الدليل الصوتي.

```csharp
public class PhoneticGuide
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | يحصل على النص الأساسي للدليل الصوتي. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | يحصل على نص روبي للدليل الصوتي. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
