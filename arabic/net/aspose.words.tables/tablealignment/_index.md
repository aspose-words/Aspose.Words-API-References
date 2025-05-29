---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Tables.TableAlignment لمحاذاة مثالية للجداول المضمنة. حسّن تنسيق مستنداتك بدقة وسهولة.
type: docs
weight: 7200
url: /ar/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

يحدد المحاذاة لجدول مضمن.

```csharp
public enum TableAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Left | `0` | تم محاذاة الجدول إلى اليسار. |
| Center | `1` | تم وضع الجدول في المنتصف. |
| Right | `2` | تم محاذاة الجدول إلى اليمين. |

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

* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
