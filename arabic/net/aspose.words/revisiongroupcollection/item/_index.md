---
title: RevisionGroupCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: تمتع بالوصول إلى مجموعات المراجعات المحددة بسهولة باستخدام خاصية RevisionGroupCollection. حسّن إدارة بياناتك بفهرسة دقيقة.
type: docs
weight: 20
url: /ar/net/aspose.words/revisiongroupcollection/item/
---
## RevisionGroupCollection indexer

يعيد مجموعة المراجعة عند الفهرس المحدد.

```csharp
public RevisionGroup this[int index] { get; }
```

## أمثلة

يوضح كيفية الحصول على مجموعة من المراجعات في مستند.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

### أنظر أيضا

* class [RevisionGroup](../../revisiongroup/)
* class [RevisionGroupCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
