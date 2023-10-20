---
title: Field.Unlink
linktitle: Unlink
articleTitle: Unlink
second_title: Aspose.Words لـ .NET
description: Field Unlink طريقة. يقوم بإلغاء ربط الحقل في C#.
type: docs
weight: 130
url: /ar/net/aspose.words.fields/field/unlink/
---
## Field.Unlink method

يقوم بإلغاء ربط الحقل.

```csharp
public bool Unlink()
```

### قيمة الإرجاع

`حقيقي` إذا تم إلغاء ربط الحقل، وإلا`خطأ شنيع` .

## ملاحظات

يستبدل الحقل بنتيجةه الأحدث.

لا يمكن إلغاء ربط بعض الحقول، مثل حقول XE (إدخال الفهرس) وحقول SEQ (التسلسل).

## أمثلة

يوضح كيفية إلغاء ربط الحقل.

```csharp
Document doc = new Document(MyDir + "Linked fields.docx");
doc.Range.Fields[1].Unlink();
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
