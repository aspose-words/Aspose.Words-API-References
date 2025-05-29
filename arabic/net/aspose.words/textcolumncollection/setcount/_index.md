---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words لـ .NET
description: قم بتحسين تخطيطك باستخدام طريقة TextColumnCollection SetCount، وقم بترتيب النص بسهولة في العدد المطلوب من الأعمدة لتحسين قابلية القراءة.
type: docs
weight: 70
url: /ar/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

يقوم بترتيب النص في العدد المحدد من أعمدة النص.

```csharp
public void SetCount(int newCount)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| newCount | Int32 | عدد الأعمدة التي سيتم ترتيب النص فيها. |

## ملاحظات

متى[`EvenlySpaced`](../evenlyspaced/) يكون`خطأ شنيع` وتزيد عدد الأعمدة، جديد[`TextColumn`](../../textcolumn/) يتم إنشاء الكائنات بعرض ومسافة صفرية. تحتاج إلى تعيين العرض والمسافة للأعمدة الجديدة.

## أمثلة

يوضح كيفية إنشاء عدة أعمدة متباعدة بشكل متساوٍ في قسم.

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
