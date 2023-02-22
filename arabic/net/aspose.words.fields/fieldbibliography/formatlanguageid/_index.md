---
title: FieldBibliography.FormatLanguageId
second_title: Aspose.Words لمراجع .NET API
description: FieldBibliography ملكية. الحصول على أو تحديد معرف اللغة المستخدم لتنسيق المصادر الببليوغرافية في المستند.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldbibliography/formatlanguageid/
---
## FieldBibliography.FormatLanguageId property

الحصول على أو تحديد معرف اللغة المستخدم لتنسيق المصادر الببليوغرافية في المستند.

```csharp
public string FormatLanguageId { get; set; }
```

### أمثلة

يوضح كيفية العمل مع حقلي CITATION و BIBLIOGRAPHY.

```csharp
// افتح مستندًا يحتوي على مصادر ببليوغرافية يمكننا العثور عليها
// Microsoft Word عبر المراجع - >; الاقتباسات وأمبير. ببليوغرافيا - >. إدارة المصادر.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// أنشئ اقتباسًا برقم الصفحة فقط ومؤلف الكتاب المشار إليه.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// نشير إلى المصادر باستخدام أسماء العلامات الخاصة بهم.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// إنشاء اقتباس أكثر تفصيلاً يستشهد بمصدرين.
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

// يمكننا استخدام حقل ببليوجرافي لعرض جميع المصادر داخل المستند.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### أنظر أيضا

* class [FieldBibliography](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldbibliography/)
* المجسم [Aspose.Words](../../../)


