---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words لـ .NET
description: StyleCollection ClearQuickStyleGallery طريقة. إزالة كافة الأنماط من لوحة Quick Style Gallery في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

إزالة كافة الأنماط من لوحة Quick Style Gallery.

```csharp
public void ClearQuickStyleGallery()
```

## أمثلة

يوضح كيفية إزالة الأنماط من لوحة Style Gallery.

```csharp
Document doc = new Document();
// لاحظ أن إزالة الأنماط تعمل فقط مع تنسيق DOCX في الوقت الحالي.
doc.Styles.ClearQuickStyleGallery();

doc.Save(ArtifactsDir + "Styles.RemoveStylesFromStyleGallery.docx");
```

### أنظر أيضا

* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
