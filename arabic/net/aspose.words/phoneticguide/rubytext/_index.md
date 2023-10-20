---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words لـ .NET
description: PhoneticGuide RubyText ملكية. الحصول على نص روبي من الدليل الصوتي في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

الحصول على نص روبي من الدليل الصوتي.

```csharp
public string RubyText { get; }
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

* class [PhoneticGuide](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
