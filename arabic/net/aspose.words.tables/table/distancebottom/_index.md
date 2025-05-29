---
title: Table.DistanceBottom
linktitle: DistanceBottom
articleTitle: DistanceBottom
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية Table DistanceBottom للتحكم في المسافة بين أسفل الجدول والنص المحيط به، مما يؤدي إلى تحسين التخطيط وسهولة القراءة.
type: docs
weight: 120
url: /ar/net/aspose.words.tables/table/distancebottom/
---
## Table.DistanceBottom property

يحصل على المسافة بين أسفل الجدول والنص المحيط بها، بالنقاط، أو يعينها.

```csharp
public double DistanceBottom { get; set; }
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
