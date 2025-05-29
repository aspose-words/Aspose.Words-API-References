---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية عرض مجموعة أعمدة النص. أدر بسهولة الأعمدة المتساوية المسافات لتحقيق تخطيط وتصميم مثاليين لمشاريعك.
type: docs
weight: 60
url: /ar/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

عندما تكون المسافة بين الأعمدة متساوية، يتم الحصول على عرض الأعمدة.

```csharp
public double Width { get; }
```

## ملاحظات

لا يكون له تأثير إلا عندما[`EvenlySpaced`](../evenlyspaced/) تم ضبطه على`حقيقي`.

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
