---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PhoneticGuide RubyText للوصول إلى نص Ruby وتحسينه لتحسين الوضوح الصوتي في تطبيقاتك.
type: docs
weight: 20
url: /ar/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

يحصل على نص روبي للدليل الصوتي.

```csharp
public string RubyText { get; }
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
