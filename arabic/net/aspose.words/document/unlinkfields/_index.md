---
title: Document.UnlinkFields
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إلغاء ربط الحقول في المستند بأكمله.
type: docs
weight: 710
url: /ar/net/aspose.words/document/unlinkfields/
---
## Document.UnlinkFields method

إلغاء ربط الحقول في المستند بأكمله.

```csharp
public void UnlinkFields()
```

### ملاحظات

يستبدل جميع الحقول في المستند بأكمله بأحدث نتائجها.

لإلغاء ارتباط الحقول في جزء معين من المستند ، استخدم[`UnlinkFields`](../../range/unlinkfields/).

### أمثلة

يوضح كيفية إلغاء ارتباط كل الحقول في المستند.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");

doc.UnlinkFields();
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


