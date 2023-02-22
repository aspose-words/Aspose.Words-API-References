---
title: MailMerge.DeleteFields
second_title: Aspose.Words لمراجع .NET API
description: MailMerge طريقة. يزيل الحقول المتعلقة بدمج المراسلات من المستند.
type: docs
weight: 170
url: /ar/net/aspose.words.mailmerging/mailmerge/deletefields/
---
## MailMerge.DeleteFields method

يزيل الحقول المتعلقة بدمج المراسلات من المستند.

```csharp
public void DeleteFields()
```

### ملاحظات

تزيل هذه الطريقة حقول MERGEFIELD و NEXT من المستند.

قد تكون هذه الطريقة مفيدة إذا كانت عملية دمج المراسلات لا تحتاج دائمًا إلى لتعبئة كافة الحقول في المستند. استخدم هذه الطريقة لإزالة كافة حقول دمج المراسلات المتبقية.

### أمثلة

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
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


