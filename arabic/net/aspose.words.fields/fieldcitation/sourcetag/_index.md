---
title: FieldCitation.SourceTag
linktitle: SourceTag
articleTitle: SourceTag
second_title: Aspose.Words لـ .NET
description: FieldCitation SourceTag ملكية. الحصول على أو تعيين قيمة تطابقبطاقة شعار قيمة العنصر للمصدر المراد إدراجه في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/fieldcitation/sourcetag/
---
## FieldCitation.SourceTag property

الحصول على أو تعيين قيمة تطابق**بطاقة شعار** قيمة العنصر للمصدر المراد إدراجه.

```csharp
public string SourceTag { get; set; }
```

## أمثلة

يوضح كيفية العمل مع حقول CITATION وBIBLIOGRAPHY.

```csharp
// افتح مستندًا يحتوي على مصادر ببليوغرافية يمكننا العثور عليها
// Microsoft Word عبر المراجع -> اقتباسات & قائمة المراجع -> إدارة المصادر.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// أنشئ اقتباسًا باستخدام رقم الصفحة ومؤلف الكتاب المشار إليه فقط.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// نشير إلى المصادر باستخدام أسماء علاماتها.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// قم بإنشاء اقتباس أكثر تفصيلاً يستشهد بمصدرين.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// يمكننا استخدام حقل الببليوغرافيا لعرض كافة المصادر داخل الوثيقة.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### أنظر أيضا

* class [FieldCitation](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
