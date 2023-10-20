---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Tables.TableAlignment تعداد. تحديد المحاذاة للجدول المضمن في C#.
type: docs
weight: 6350
url: /ar/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

تحديد المحاذاة للجدول المضمن.

```csharp
public enum TableAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Left | `0` | تمت محاذاة الجدول إلى اليسار. |
| Center | `1` | الجدول في المنتصف. |
| Right | `2` | تمت محاذاة الجدول إلى اليمين. |

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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
