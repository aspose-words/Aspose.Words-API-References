---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words لـ .NET
description: خصّص جدول بياناتك باستخدام خاصية DeleteCellColor في RevisionOptions. حدّد بسهولة لونًا فريدًا للخلايا المحذوفة، مما يُحسّن الوضوح والتنظيم.
type: docs
weight: 20
url: /ar/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

يسمح بتحديد اللون الذي سيتم استخدامه للخلايا المحذوفةDeletion . القيمة الافتراضية هيPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
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
