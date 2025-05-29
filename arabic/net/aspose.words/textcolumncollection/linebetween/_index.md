---
title: TextColumnCollection.LineBetween
linktitle: LineBetween
articleTitle: LineBetween
second_title: Aspose.Words لـ .NET
description: حسّن تخطيطك باستخدام خاصية TextColumnCollection LineBetween. فعّل الخطوط العمودية بين الأعمدة لمظهر أنيق ومنظم.
type: docs
weight: 40
url: /ar/net/aspose.words/textcolumncollection/linebetween/
---
## TextColumnCollection.LineBetween property

عندما`حقيقي` ، يضيف خطًا رأسيًا بين الأعمدة.

```csharp
public bool LineBetween { get; set; }
```

## أمثلة

يوضح كيفية فصل الأعمدة باستخدام خط عمودي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتكوين كائن PageSetup الخاص بالقسم الحالي لتقسيم النص إلى عدة أعمدة.
// قم بضبط خاصية "LineBetween" على "true" لوضع خط فاصل بين الأعمدة.
// قم بضبط الخاصية "LineBetween" على "false" لترك المسافة بين الأعمدة فارغة.
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.LineBetween = lineBetween;
columns.SetCount(3);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 3.");

doc.Save(ArtifactsDir + "PageSetup.VerticalLineBetweenColumns.docx");
```

### أنظر أيضا

* class [TextColumnCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
