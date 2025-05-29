---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Tables.PreferredWidthType enum. حدّد بسهولة قياسات عرض الجدول والخليّة لتنسيق المستندات بدقة.
type: docs
weight: 7150
url: /ar/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

يحدد وحدة القياس للعرض المفضل للجدول أو الخلية.

```csharp
public enum PreferredWidthType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `1` | لم يتم تحديد العرض المُفضّل. يُحدَّد العرض الفعلي للجدول أو الخلية إما باستخدام العرض الصريح، أو سيتم تحديده تلقائيًا بواسطة خوارزمية تخطيط الجدول عند عرضه، وذلك وفقًا لإعداد الملاءمة التلقائية للجدول. |
| Percent | `2` | قم بقياس عرض العنصر الحالي باستخدام نسبة مئوية محددة. |
| Points | `3` | قم بقياس عرض العنصر الحالي باستخدام عدد محدد من النقاط (1/72 بوصة). |

## أمثلة

يوضح كيفية التحقق من نوع العرض وقيمة خلية الجدول المفضلة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### أنظر أيضا

* class [PreferredWidth](../preferredwidth/)
* مساحة الاسم [Aspose.Words.Tables](../../aspose.words.tables/)
* المجسم [Aspose.Words](../../)
