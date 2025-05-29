---
title: FieldCitation.SuppressYear
linktitle: SuppressYear
articleTitle: SuppressYear
second_title: Aspose.Words لـ .NET
description: أدر تفاصيل الاستشهادات باستخدام خاصية FieldCitation SuppressYear. تحكم بسهولة في عرض السنة لتحسين وضوح مراجعك.
type: docs
weight: 100
url: /ar/net/aspose.words.fields/fieldcitation/suppressyear/
---
## FieldCitation.SuppressYear property

يحصل على أو يحدد ما إذا كان سيتم حذف معلومات السنة من الاستشهاد.

```csharp
public bool SuppressYear { get; set; }
```

## أمثلة

يوضح كيفية العمل مع حقول الاستشهادات والمراجع.

```csharp
// افتح مستندًا يحتوي على المصادر الببليوغرافية التي يمكننا العثور عليها في
// Microsoft Word عبر المراجع -> الاستشهادات والمراجع -> إدارة المصادر.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// قم بإنشاء استشهاد باستخدام رقم الصفحة ومؤلف الكتاب المشار إليه فقط.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

//نشير إلى المصادر باستخدام أسماء علاماتها.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// قم بإنشاء استشهاد أكثر تفصيلاً يستشهد بمصدرين.
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

// يمكننا استخدام حقل المراجع لعرض جميع المصادر الموجودة داخل المستند.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### أنظر أيضا

* class [FieldCitation](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
