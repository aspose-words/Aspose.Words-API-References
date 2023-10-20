---
title: ControlChar.LineFeedChar
linktitle: LineFeedChar
articleTitle: LineFeedChar
second_title: Aspose.Words لـ .NET
description: ControlChar LineFeedChar مجال. حرف تغذية السطر char10 أو n في C#.
type: docs
weight: 150
url: /ar/net/aspose.words/controlchar/linefeedchar/
---
## ControlChar.LineFeedChar field

حرف تغذية السطر: (char)10 أو "\n".

```csharp
public const char LineFeedChar;
```

## أمثلة

يوضح كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف مسافة عادية.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// أضف NBSP، وهي مسافة غير منقسمة.
// على عكس المساحة العادية، لا يمكن أن تحتوي هذه المساحة على فاصل أسطر تلقائي في موضعها.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// أضف حرف علامة التبويب.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// أضف فاصل أسطر.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// أضف سطرًا جديدًا وابدأ فقرة جديدة.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// حرف تغذية السطر له نسختان.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// يمكن تمثيل أحرف الإرجاع وخلاصات الأسطر معًا بحرف واحد.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// أضف فاصل فقرة، والذي سيبدأ فقرة جديدة.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// أضف فاصل قسم. وهذا لا يؤدي إلى إنشاء قسم أو فقرة جديدة.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// أضف فاصل الصفحات.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// فاصل الصفحة هو نفس قيمة فاصل القسم.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// أدخل قسمًا جديدًا، ثم اضبط عدد أعمدته على اثنين.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// يمكننا استخدام حرف التحكم لتحديد النقطة التي ينتقل فيها النص إلى العمود التالي.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// هناك نظيرات للحرف والسلسلة لمعظم الشخصيات.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### أنظر أيضا

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
