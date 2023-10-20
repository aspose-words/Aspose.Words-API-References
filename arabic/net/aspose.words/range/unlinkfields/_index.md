---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words لـ .NET
description: Range UnlinkFields طريقة. إلغاء ربط الحقول في هذا النطاق في C#.
type: docs
weight: 110
url: /ar/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

إلغاء ربط الحقول في هذا النطاق.

```csharp
public void UnlinkFields()
```

## ملاحظات

يستبدل كافة الحقول الموجودة في هذا النطاق بأحدث نتائجها.

لإلغاء ربط الحقول في استخدام المستند بأكمله`UnlinkFields`.

## أمثلة

يوضح كيفية إلغاء ربط كافة الحقول في النطاق.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

Section newSection = (Section)doc.Sections[0].Clone(true);
doc.Sections.Add(newSection);

doc.Sections[1].Range.UnlinkFields();
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
