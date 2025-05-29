---
title: Range.UnlinkFields
linktitle: UnlinkFields
articleTitle: UnlinkFields
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Range UnlinkFields لإلغاء ربط الحقول في نطاق مستندك بسهولة، مما يحسن سير عملك وإدارة المستندات.
type: docs
weight: 120
url: /ar/net/aspose.words/range/unlinkfields/
---
## Range.UnlinkFields method

إلغاء ربط الحقول في هذا النطاق.

```csharp
public void UnlinkFields()
```

## ملاحظات

استبدال كافة الحقول في هذا النطاق بنتائجها الأحدث.

لإلغاء ربط الحقول في المستند بأكمله، استخدم`UnlinkFields`.

## أمثلة

يوضح كيفية إلغاء ربط جميع الحقول في نطاق معين.

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
