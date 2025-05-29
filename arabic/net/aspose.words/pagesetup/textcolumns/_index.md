---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup TextColumns، وتمكن من الوصول إلى مجموعة متعددة الاستخدامات من أعمدة النص لتحسين تخطيط مستندك وتنسيقه بسهولة.
type: docs
weight: 420
url: /ar/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

يعيد مجموعة تمثل مجموعة أعمدة النص.

```csharp
public TextColumnCollection TextColumns { get; }
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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
