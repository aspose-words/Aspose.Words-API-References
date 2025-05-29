---
title: PageSetup.PageNumberStyle
linktitle: PageNumberStyle
articleTitle: PageNumberStyle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageNumberStyle في PageSetup لتخصيص تنسيق رقم الصفحة بسهولة لتحسين عرض المستند ووضوحه.
type: docs
weight: 320
url: /ar/net/aspose.words/pagesetup/pagenumberstyle/
---
## PageSetup.PageNumberStyle property

يحصل على تنسيق رقم الصفحة أو يعينه.

```csharp
public NumberStyle PageNumberStyle { get; set; }
```

## أمثلة

يوضح كيفية إعداد ترقيم الصفحات في قسم.

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

// نقل منشئ المستند إلى العنوان الأساسي للقسم الأول،
// والتي سيتم عرضها في كل صفحة في هذا القسم.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// أدخل حقل PAGE، والذي سيعرض رقم الصفحة الحالية.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول الصفحة من 5.
// قم أيضًا بتكوين جميع حقول الصفحة لعرض أرقام صفحاتها باستخدام الأرقام الرومانية الكبيرة.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// قم بإنشاء رأس أساسي آخر للقسم الثاني، مع حقل PAGE آخر.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// قم بتكوين القسم بحيث يبدأ عدد الصفحات التي تعرضها حقول الصفحة من 10.
// قم أيضًا بتكوين جميع حقول الصفحة لعرض أرقام صفحاتها باستخدام الأرقام العربية.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### أنظر أيضا

* enum [NumberStyle](../../numberstyle/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
