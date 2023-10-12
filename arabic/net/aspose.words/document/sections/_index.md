---
title: Document.Sections
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. إرجاع مجموعة تمثل كافة الأقسام في المستند.
type: docs
weight: 370
url: /ar/net/aspose.words/document/sections/
---
## Document.Sections property

إرجاع مجموعة تمثل كافة الأقسام في المستند.

```csharp
public SectionCollection Sections { get; }
```

### أمثلة

يوضح كيفية إضافة وإزالة الأقسام في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// احذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// إلحاق نسخة مما هو الآن القسم الأول بنهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

يوضح كيفية تحديد كيفية فصل قسم جديد عن القسم السابق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// تحدد أنواع الفواصل المقطعية كيفية فصل قسم جديد عن القسم السابق.
// فيما يلي خمسة أنواع من فواصل الأقسام.
// 1 - يبدأ القسم التالي في صفحة جديدة:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - يبدأ القسم التالي في الصفحة الحالية:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - يبدأ القسم التالي في صفحة زوجية جديدة:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - يبدأ القسم التالي في صفحة فردية جديدة:
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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


