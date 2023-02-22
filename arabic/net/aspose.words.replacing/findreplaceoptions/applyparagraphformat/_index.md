---
title: FindReplaceOptions.ApplyParagraphFormat
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. تم تطبيق تنسيق الفقرة على المحتوى الجديد.
type: docs
weight: 30
url: /ar/net/aspose.words.replacing/findreplaceoptions/applyparagraphformat/
---
## FindReplaceOptions.ApplyParagraphFormat property

تم تطبيق تنسيق الفقرة على المحتوى الجديد.

```csharp
public ParagraphFormat ApplyParagraphFormat { get; }
```

### أمثلة

يوضح كيفية إضافة تنسيق إلى الفقرات التي عثرت فيها عملية البحث والاستبدال على تطابقات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط خاصية "Alignment" على "ParagraphAlignment.Right" لمحاذاة كل فقرة إلى اليمين
// الذي يحتوي على تطابق تجده عملية البحث والاستبدال.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// استبدل كل نقطة توقف مباشرة قبل فاصل الفقرة بعلامة تعجب.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### أنظر أيضا

* class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


