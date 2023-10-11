---
title: Table.DistanceRight
second_title: Aspose.Words لمراجع .NET API
description: Table ملكية. الحصول على أو تعيين المسافة بين يمين الجدول والنص المحيط بالنقاط.
type: docs
weight: 140
url: /ar/net/aspose.words.tables/table/distanceright/
---
## Table.DistanceRight property

الحصول على أو تعيين المسافة بين يمين الجدول والنص المحيط بالنقاط.

```csharp
public double DistanceRight { get; set; }
```

### أمثلة

يوضح كيفية ضبط المسافة بين حدود الجدول والنص.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];
Assert.AreEqual(25.9d, table.DistanceTop);
Assert.AreEqual(25.9d, table.DistanceBottom);
Assert.AreEqual(17.3d, table.DistanceLeft);
Assert.AreEqual(17.3d, table.DistanceRight);

 // اضبط المسافة بين الجدول والنص المحيط.
table.DistanceLeft = 24;
table.DistanceRight = 24;
table.DistanceTop = 3;
table.DistanceBottom = 3;

doc.Save(ArtifactsDir + "Table.DistanceBetweenTableAndText.docx");
```

### أنظر أيضا

* class [Table](../)
* مساحة الاسم [Aspose.Words.Tables](../../table/)
* المجسم [Aspose.Words](../../../)


