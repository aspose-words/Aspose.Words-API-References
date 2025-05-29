---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: Aspose.Words لـ .NET
description: استكشف خاصية أقسام المستند للوصول إلى مجموعة كاملة من كافة أقسام المستند، مما يعمل على تحسين تنظيم المحتوى والتنقل فيه.
type: docs
weight: 390
url: /ar/net/aspose.words/document/sections/
---
## Document.Sections property

يعيد مجموعة تمثل جميع الأقسام في المستند.

```csharp
public SectionCollection Sections { get; }
```

## أمثلة

يوضح كيفية إضافة أقسام وإزالتها في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

//حذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// قم بإضافة نسخة من القسم الأول إلى نهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

يوضح كيفية تحديد كيفية فصل القسم الجديد عن القسم السابق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// تحدد أنواع فواصل الأقسام كيفية فصل القسم الجديد عن القسم السابق.
// فيما يلي خمسة أنواع من فواصل الأقسام.
// 1 - يبدأ القسم التالي على صفحة جديدة:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - يبدأ القسم التالي في الصفحة الحالية:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - يبدأ القسم التالي على صفحة زوجية جديدة:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - يبدأ القسم التالي على صفحة فردية جديدة:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - يبدأ القسم التالي في عمود جديد:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### أنظر أيضا

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
