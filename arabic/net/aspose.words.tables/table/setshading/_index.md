---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مظهر الجدول الخاص بك باستخدام طريقة SetShading، مما يسمح لك بتطبيق قيم تظليل مخصصة للحصول على مظهر أنيق واحترافي.
type: docs
weight: 450
url: /ar/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

تعيين التظليل إلى القيم المحددة على الجدول بأكمله.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| texture | TextureIndex | الملمس المراد تطبيقه. |
| foregroundColor | Color | لون الملمس. |
| backgroundColor | Color | لون تعبئة الخلفية. |

## أمثلة

يوضح كيفية تطبيق حدود تفصيلية على جدول.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

//محاذاة الجدول إلى منتصف الصفحة.
table.Alignment = TableAlignment.Center;

// قم بمسح أي حدود وتظليل موجود من الجدول.
table.ClearBorders();
table.ClearShading();

//أضف حدودًا خضراء إلى مخطط الجدول.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// املأ الخلايا بلون أخضر فاتح.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### أنظر أيضا

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
