---
title: TxtSaveOptionsBase.ParagraphBreak
second_title: Aspose.Words لمراجع .NET API
description: TxtSaveOptionsBase ملكية. يحدد السلسلة التي سيتم استخدامها كفاصل فقرة عند التصدير بتنسيقات نصية.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

يحدد السلسلة التي سيتم استخدامها كفاصل فقرة عند التصدير بتنسيقات نصية.

```csharp
public string ParagraphBreak { get; set; }
```

### ملاحظات

النظام الأساسي[`CrLf`](../../../aspose.words/controlchar/crlf/).

### أمثلة

يوضح كيفية حفظ مستند .txt مع فاصل فقرة مخصص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// قم بإنشاء كائن "TxtSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية حفظ المستند على نص عادي.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// اضبط "ParagraphBreak" على قيمة مخصصة نرغب في وضعها في نهاية كل فقرة.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### أنظر أيضا

* class [TxtSaveOptionsBase](../)
* مساحة الاسم [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* المجسم [Aspose.Words](../../../)


