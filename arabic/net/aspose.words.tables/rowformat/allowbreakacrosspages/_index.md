---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية RowFormat AllowBreakAcrossPages، وقم بتمكين تدفق النص بشكل سلس في صفوف الجدول عبر فواصل الصفحات لتحسين إمكانية القراءة والعرض.
type: docs
weight: 10
url: /ar/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

صحيح إذا كان من المسموح تقسيم النص الموجود في صف الجدول عبر فاصل الصفحة.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## أمثلة

يوضح كيفية تعطيل تقسيم الصفوف عبر الصفحات لكل صف في الجدول.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// اضبط خاصية "AllowBreakAcrossPages" على "false" للاحتفاظ بالصف
// في قطعة واحدة إذا كان الجدول يمتد على صفحتين، والتي تنقسم على طول هذا الصف.
// إذا كان الصف كبيرًا جدًا بحيث لا يتناسب مع صفحة واحدة، فسوف يقوم Microsoft Word بدفعه إلى الصفحة التالية.
// قم بتعيين الخاصية "AllowBreakAcrossPages" إلى "true" للسماح بتقسيم الصف عبر صفحتين.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### أنظر أيضا

* class [RowFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
