---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words لـ .NET
description: خصّص مظهر جدولك باستخدام طريقة SetBorder - اضبط نمط الخط وعرضه ولونه لمظهر احترافي. حسّن تصميمك اليوم!
type: docs
weight: 430
url: /ar/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

تعيين حدود الجدول المحددة إلى نمط الخط والعرض واللون المحددين.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| borderType | BorderType | حدود الجدول للتغيير. |
| lineStyle | LineStyle | نمط الخط المراد تطبيقه. |
| lineWidth | Double | عرض الخط الذي يجب تعيينه (بالنقاط). |
| color | Color | اللون الذي يجب استخدامه للحدود. |
| isOverrideCellBorders | Boolean | متى`حقيقي`يؤدي ذلك إلى إزالة جميع حدود الخلايا الصريحة الموجودة. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
