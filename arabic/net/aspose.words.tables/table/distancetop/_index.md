---
title: Table.DistanceTop
linktitle: DistanceTop
articleTitle: DistanceTop
second_title: Aspose.Words لـ .NET
description: اضبط المسافة بين سطح طاولتك والنص المحيط بها بسهولة. حسّن تصميمك لمظهر أنيق واحترافي مع DistanceTop!
type: docs
weight: 150
url: /ar/net/aspose.words.tables/table/distancetop/
---
## Table.DistanceTop property

يحصل على المسافة بين أعلى الجدول والنص المحيط به، بالنقاط، أو يعينها.

```csharp
public double DistanceTop { get; set; }
```

## أمثلة

يوضح كيفية تعيين المسافة بين حدود الجدول والنص.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

// تعيين المسافة بين الجدول والنص المحيط به.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
