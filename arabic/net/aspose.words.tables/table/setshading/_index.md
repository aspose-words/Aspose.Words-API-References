---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words لـ .NET
description: Table SetShading طريقة. يضبط التظليل على القيم المحددة في الجدول بأكمله في C#.
type: docs
weight: 430
url: /ar/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

يضبط التظليل على القيم المحددة في الجدول بأكمله.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| texture | TextureIndex | الملمس المطلوب تطبيقه. |
| foregroundColor | Color | لون الملمس. |
| backgroundColor | Color | لون تعبئة الخلفية. |

## أمثلة

يوضح كيفية تطبيق حدود المخطط التفصيلي على جدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// قم بمحاذاة الجدول إلى منتصف الصفحة.
table.Alignment = TableAlignment.Center;

// امسح أي حدود وتظليل موجود من الجدول.
table.ClearBorders();
table.ClearShading();

// أضف حدودًا خضراء إلى مخطط الجدول.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// املأ الخلايا بلون أخضر فاتح خالص.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### أنظر أيضا

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
