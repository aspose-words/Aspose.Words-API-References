---
title: TxtSaveOptionsBase.ParagraphBreak
linktitle: ParagraphBreak
articleTitle: ParagraphBreak
second_title: Aspose.Words لـ .NET
description: TxtSaveOptionsBase ParagraphBreak ملكية. يحدد السلسلة التي سيتم استخدامها كفواصل فقرات عند التصدير بتنسيقات نصية في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

يحدد السلسلة التي سيتم استخدامها كفواصل فقرات عند التصدير بتنسيقات نصية.

```csharp
public string ParagraphBreak { get; set; }
```

## ملاحظات

القيمة الافتراضية هي[`CrLf`](../../../aspose.words/controlchar/crlf/).

## أمثلة

يوضح كيفية حفظ مستند .txt مع فاصل فقرات مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// قم بإنشاء كائن "TxtSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية حفظ المستند إلى نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// قم بتعيين "ParagraphBreak" على قيمة مخصصة نرغب في وضعها في نهاية كل فقرة.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### أنظر أيضا

* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
