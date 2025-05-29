---
title: StyleCollection.ClearQuickStyleGallery
linktitle: ClearQuickStyleGallery
articleTitle: ClearQuickStyleGallery
second_title: Aspose.Words لـ .NET
description: امسح أنماطك بسهولة من معرض الأنماط السريع باستخدام طريقة ClearQuickStyleGallery من StyleCollection. بسّط عملية التصميم الخاصة بك اليوم!
type: docs
weight: 80
url: /ar/net/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection.ClearQuickStyleGallery method

يزيل جميع الأنماط من لوحة معرض الأنماط السريعة.

```csharp
public void ClearQuickStyleGallery()
```

## أمثلة

يوضح كيفية إزالة الأنماط من لوحة معرض الأنماط.

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
