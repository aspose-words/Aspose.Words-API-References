---
title: PageSetup.TextColumns
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. إرجاع مجموعة تمثل مجموعة أعمدة النص.
type: docs
weight: 420
url: /ar/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

إرجاع مجموعة تمثل مجموعة أعمدة النص.

```csharp
public TextColumnCollection TextColumns { get; }
```

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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


