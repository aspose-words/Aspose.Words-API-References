---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words لـ .NET
description: TextColumnCollection SetCount طريقة. ترتيب النص في العدد المحدد من أعمدة النص في C#.
type: docs
weight: 70
url: /ar/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

ترتيب النص في العدد المحدد من أعمدة النص.

```csharp
public void SetCount(int newCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| newCount | Int32 | عدد الأعمدة التي سيتم ترتيب النص فيها. |

## ملاحظات

متى[`EvenlySpaced`](../evenlyspaced/) يكون`خطأ شنيع` وقمت بزيادة عدد الأعمدة new[`TextColumn`](../../textcolumn/) يتم إنشاء الكائنات بعرض وتباعد صفر. تحتاج إلى ضبط العرض والتباعد للأعمدة الجديدة.

## أمثلة

يوضح كيفية إنشاء عدة أعمدة متباعدة بشكل متساوٍ في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### أنظر أيضا

* class [TextColumnCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
