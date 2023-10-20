---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words لـ .NET
description: MailMerge DeleteFields طريقة. إزالة الحقول المرتبطة بدمج البريد من المستند في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

إزالة الحقول المرتبطة بدمج البريد من المستند.

```csharp
public void DeleteFields()
```

## ملاحظات

تقوم هذه الطريقة بإزالة حقول MERGEFIELD وNEXT من المستند.

قد تكون هذه الطريقة مفيدة إذا كانت عملية دمج البريد لديك لا تحتاج دائمًا إلى لملء كافة الحقول في المستند. استخدم هذه الطريقة لإزالة كافة حقول دمج المراسلات المتبقية .

## أمثلة

يوضح كيفية حذف كافة MERGEFIELDs من مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.Writeln(",");
builder.Writeln("Greetings!");

Assert.AreEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!", 
    doc.GetText().Trim());

doc.MailMerge.DeleteFields();

Assert.AreEqual("Dear  ,\rGreetings!", doc.GetText().Trim());
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
