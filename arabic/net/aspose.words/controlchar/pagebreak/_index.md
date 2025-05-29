---
title: ControlChar.PageBreak
linktitle: PageBreak
articleTitle: PageBreak
second_title: Aspose.Words لـ .NET
description: اكتشف حقل فواصل الصفحات ControlChar، وأدر فواصل الصفحات بكفاءة باستخدام حرف x000c. بسّط تنسيق مستنداتك اليوم!
type: docs
weight: 200
url: /ar/net/aspose.words/controlchar/pagebreak/
---
## ControlChar.PageBreak field

حرف فاصل الصفحة : "\x000c" أو "\f". لاحظ أن قيمته هي نفسها[`SectionBreak`](../sectionbreak/) .

```csharp
public static readonly string PageBreak;
```

## أمثلة

يوضح كيفية إضافة أحرف تحكم مختلفة إلى مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أضف مسافة عادية.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// أضف NBSP، وهي مسافة غير قابلة للكسر.
// على عكس المساحة العادية، لا يمكن لهذه المساحة أن تحتوي على فاصل سطر تلقائي في موضعها.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

//أضف حرف الجدولة.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

//أضف فاصلًا للسطر.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

//أضف سطرًا جديدًا وابدأ فقرة جديدة.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// تحتوي حرف تغذية السطر على نسختين.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

//يمكن تمثيل إرجاعات العربة وتغذية السطر معًا بحرف واحد.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

//أضف فاصل فقرة، مما سيؤدي إلى بدء فقرة جديدة.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// أضف فاصلًا للقسم. هذا لا يُنشئ قسمًا أو فقرة جديدة.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

//أضف فاصل الصفحة.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

//قيمة كسر الصفحة هي نفس قيمة كسر القسم.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// قم بإدراج قسم جديد، ثم قم بتعيين عدد أعمدته إلى اثنين.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

//يمكننا استخدام حرف التحكم لتحديد النقطة التي ينتقل عندها النص إلى العمود التالي.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// هناك نظراء char و string لمعظم الأحرف.
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
