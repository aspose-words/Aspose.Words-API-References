---
title: Table.SetBorder
second_title: Aspose.Words لمراجع .NET API
description: Table طريقة. يضبط حدود الجدول المحدد على نمط الخط المحدد والعرض واللون.
type: docs
weight: 430
url: /ar/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

يضبط حدود الجدول المحدد على نمط الخط المحدد والعرض واللون.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| borderType | BorderType | حدود الجدول للتغيير. |
| lineStyle | LineStyle | نمط الخط المطلوب تطبيقه. |
| lineWidth | Double | عرض الخط المراد ضبطه (بالنقاط). |
| color | Color | اللون الذي سيتم استخدامه للحدود. |
| isOverrideCellBorders | Boolean | متى`حقيقي`، يؤدي إلى إزالة كافة حدود الخلايا الصريحة الموجودة. |

### أمثلة

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


