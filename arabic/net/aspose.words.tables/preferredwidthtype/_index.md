---
title: Enum PreferredWidthType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Tables.PreferredWidthType تعداد. يحدد وحدة القياس للعرض المفضل للجدول أو الخلية.
type: docs
weight: 6300
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
| Auto | `1` | لم يتم تحديد العرض المفضل. يتم تحديد العرض الفعلي للجدول أو الخلية باستخدام العرض الصريح أو سيتم تحديد تلقائيًا بواسطة خوارزمية تخطيط الجدول عند عرض الجدول، اعتمادًا على إعداد الاحتواء التلقائي للجدول. |
| Percent | `2` | قياس عرض العنصر الحالي باستخدام نسبة مئوية محددة. |
| Points | `3` | قياس عرض العنصر الحالي باستخدام عدد محدد من النقاط (1/72 بوصة). |

### أمثلة

يوضح كيفية التحقق من نوع العرض المفضل وقيمة خلية الجدول.

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


