---
title: Document.VersionsCount
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. الحصول على عدد إصدارات المستند التي تم تخزينها في مستند DOC.
type: docs
weight: 460
url: /ar/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

الحصول على عدد إصدارات المستند التي تم تخزينها في مستند DOC.

```csharp
public int VersionsCount { get; }
```

### ملاحظات

يتم الوصول إلى الإصدارات في Microsoft Word عبر قائمة الملفات/الإصدارات. يدعم Microsoft Word إصدارات فقط لملفات DOC.

تسمح هذه الخاصية باكتشاف ما إذا كانت هناك إصدارات مستند مخزنة في document هذا قبل فتحه في Aspose.Words. لا يوفر Aspose.Words أي دعم آخر لإصدارات المستند. إذا قمت بحفظ هذا المستند باستخدام Aspose.Words، فسيتم حفظ المستند بدون إصدارات.

### أمثلة

يوضح كيفية العمل مع ميزة عدد الإصدارات لمستندات Microsoft Word الأقدم.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// يمكننا قراءة هذه الخاصية للمستند، لكن لا يمكننا الحفاظ عليها أثناء الحفظ.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


