---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words لـ .NET
description: خصّص جدول بياناتك باستخدام خاصية InsertCellColor في RevisionOptions. اختر اللون المُفضّل للخلايا المُدرجة - اللون الافتراضي هو الأزرق!
type: docs
weight: 50
url: /ar/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

يسمح بتحديد اللون الذي سيتم استخدامه للخلايا المدرجةInsertion . القيمة الافتراضية هيBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
```

## أمثلة

يوضح كيفية العمل مع لون مراجعة الخلية للإدراج/الحذف.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### أنظر أيضا

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
