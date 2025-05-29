---
title: MailMerge.DeleteFields
linktitle: DeleteFields
articleTitle: DeleteFields
second_title: Aspose.Words لـ .NET
description: قم بتبسيط مستنداتك بسهولة باستخدام طريقة MailMerge DeleteFields، وإزالة حقول دمج البريد غير الضرورية للحصول على نتائج أنظف وأكثر احترافية.
type: docs
weight: 170
url: /ar/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

يزيل الحقول المرتبطة بدمج البريد من المستند.

```csharp
public void DeleteFields()
```

## ملاحظات

تؤدي هذه الطريقة إلى إزالة الحقلين MERGEFIELD وNEXT من المستند.

قد تكون هذه الطريقة مفيدة إذا لم تكن عملية دمج البريد لديك تتطلب دائمًا استخدام x000d_ لملء جميع حقول المستند. استخدم هذه الطريقة لإزالة جميع حقول دمج البريد المتبقية.

## أمثلة

يوضح كيفية حذف جميع MERGEFIELDs من مستند.

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
