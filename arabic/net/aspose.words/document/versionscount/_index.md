---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Document VersionsCount لتتبع عدد إصدارات المستندات المخزنة في ملفات DOC بسهولة لتحسين الإدارة والتنظيم.
type: docs
weight: 480
url: /ar/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

يحصل على عدد إصدارات المستند التي تم تخزينها في مستند DOC.

```csharp
public int VersionsCount { get; }
```

## ملاحظات

يمكن الوصول إلى إصدارات Microsoft Word عبر قائمة "ملف/إصدارات". يدعم Microsoft Word إصدارات x000d_ فقط لملفات DOC.

تتيح هذه الخاصية اكتشاف وجود إصدارات من المستندات مخزنة في ملف document هذا قبل فتحه في Aspose.Words. لا يوفر Aspose.Words أي دعم آخر لإصدارات المستندات. إذا حفظت هذا المستند باستخدام Aspose.Words، فسيتم حفظه بدون إصدارات.

## أمثلة

يوضح كيفية العمل مع ميزة عدد الإصدارات الخاصة بمستندات Microsoft Word القديمة.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// يمكننا قراءة هذه الخاصية من المستند، ولكن لا يمكننا الحفاظ عليها أثناء الحفظ.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
