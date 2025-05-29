---
title: HeaderFooterType Enum
linktitle: HeaderFooterType
articleTitle: HeaderFooterType
second_title: Aspose.Words لـ .NET
description: اكتشف عداد Aspose.Words.HeaderFooterType للتعرف بسهولة على أنواع الرؤوس والتذييلات في مستندات Word. حسّن معالجة مستنداتك اليوم!
type: docs
weight: 3550
url: /ar/net/aspose.words/headerfootertype/
---
## HeaderFooterType enumeration

يحدد نوع الرأس أو التذييل الموجود في ملف Word.

```csharp
public enum HeaderFooterType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| HeaderEven | `0` | رأس الصفحة للصفحات ذات الأرقام الزوجية. |
| HeaderPrimary | `1` | رأس الصفحة الأساسي، ويُستخدم أيضًا للصفحات ذات الأرقام الفردية. |
| FooterEven | `2` | تذييل للصفحات ذات الأرقام الزوجية. |
| FooterPrimary | `3` | التذييل الأساسي، ويُستخدم أيضًا للصفحات ذات الأرقام الفردية. |
| HeaderFirst | `4` | رأس الصفحة الأولى من القسم. |
| FooterFirst | `5` | تذييل الصفحة الأولى من القسم. |

## أمثلة

يوضح كيفية إنشاء الرؤوس والتذييلات في مستند باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد أننا نريد رؤوسًا وتذييلات مختلفة للصفحات الأولى والزوجية والفردية.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// قم بإنشاء الرؤوس، ثم أضف ثلاث صفحات إلى المستند لعرض كل نوع من أنواع الرؤوس.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
