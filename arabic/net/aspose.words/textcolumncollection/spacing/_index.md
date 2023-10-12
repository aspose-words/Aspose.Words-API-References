---
title: TextColumnCollection.Spacing
second_title: Aspose.Words لمراجع .NET API
description: TextColumnCollection ملكية. عندما تكون الأعمدة متباعدة بالتساوي يتم الحصول على مقدار المسافة بين كل عمود أو تعيينه بالنقاط.
type: docs
weight: 50
url: /ar/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

عندما تكون الأعمدة متباعدة بالتساوي، يتم الحصول على مقدار المسافة بين كل عمود أو تعيينه بالنقاط.

```csharp
public double Spacing { get; set; }
```

### ملاحظات

له تأثير فقط عندما[`EvenlySpaced`](../evenlyspaced/) تم ضبطه على`حقيقي` .

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../textcolumncollection/)
* المجسم [Aspose.Words](../../../)


