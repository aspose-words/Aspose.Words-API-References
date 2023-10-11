---
title: PageSetup.RestartPageNumbering
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. صحيح إذا تم إعادة تشغيل ترقيم الصفحات في بداية القسم.
type: docs
weight: 360
url: /ar/net/aspose.words/pagesetup/restartpagenumbering/
---
## PageSetup.RestartPageNumbering property

صحيح إذا تم إعادة تشغيل ترقيم الصفحات في بداية القسم.

```csharp
public bool RestartPageNumbering { get; set; }
```

### ملاحظات

إذا تم التعيين على`خطأ شنيع` ، ال`RestartPageNumbering` سوف تتجاوز الخاصية the [`PageStartingNumber`](../pagestartingnumber/) الخاصية بحيث يستمر ترقيم الصفحات من القسم السابق.

### أمثلة

يوضح كيفية إعداد ترقيم الصفحات في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// انقل أداة إنشاء المستندات إلى الرأس الأساسي للقسم الأول،
// الذي ستعرضه كل صفحة في هذا القسم.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// أدخل حقل الصفحة، والذي سيعرض رقم الصفحة الحالية.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول PAGE من 5.
// أيضًا، قم بتكوين كافة حقول PAGE لعرض أرقام الصفحات الخاصة بها باستخدام الأرقام الرومانية الكبيرة.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// أنشئ رأسًا أساسيًا آخر للقسم الثاني، مع حقل PAGE آخر.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول PAGE من 10.
// أيضًا، قم بتكوين جميع حقول PAGE لعرض أرقام صفحاتها باستخدام الأرقام العربية.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


