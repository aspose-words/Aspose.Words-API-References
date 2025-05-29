---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextColumnCollection Spacing، وأدر مسافات الأعمدة بسهولة بالنقاط للحصول على تصميم أنيق واحترافي. حسّن تصميمك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

عندما تكون المسافة بين الأعمدة متساوية، يتم الحصول على مقدار المسافة بين كل عمود بالنقاط أو تعيينه.

```csharp
public double Spacing { get; set; }
```

## ملاحظات

له تأثير فقط عندما[`EvenlySpaced`](../evenlyspaced/) تم ضبطه على`حقيقي` .

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
