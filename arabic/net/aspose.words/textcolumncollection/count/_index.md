---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count الخاصة بـ TextColumnCollection للوصول بسهولة إلى عدد الأعمدة في قسم المستند لديك لتحسين التحكم في التخطيط.
type: docs
weight: 10
url: /ar/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

يحصل على عدد الأعمدة في قسم المستند.

```csharp
public int Count { get; }
```

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
