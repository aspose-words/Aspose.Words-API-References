---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words لـ .NET
description: قم بإلغاء قفل التكامل السلس باستخدام طريقة Open من ComHelper، مما يتيح تحميل المستندات بسهولة من الملفات لتطبيقات COM الخاصة بك.
type: docs
weight: 20
url: /ar/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

يسمح لتطبيق COM بتحميل[`Document`](../../document/) من ملف.

```csharp
public Document Open(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند الذي سيتم تحميله. |

### قيمة الإرجاع

أ[`Document`](../../document/) كائن يمثل مستند Word.

## ملاحظات

هذه الطريقة هي نفس استدعاء[`Document`](../../document/) منشئ مع معلمة اسم الملف.

## أمثلة

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

يوضح كيفية فتح المستندات باستخدام فئة ComHelper.

```csharp
// تسمح لنا فئة ComHelper بتحميل المستندات من داخل عملاء COM.
ComHelper comHelper = new ComHelper();

// 1 - استخدام اسم ملف النظام المحلي:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - من مجرى:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### أنظر أيضا

* class [Document](../../document/)
* class [ComHelper](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

يسمح لتطبيق COM بالتحميل[`Document`](../../document/) من مجرى.

```csharp
public Document Open(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | كائن دفق .NET يحتوي على المستند الذي سيتم تحميله. |

### قيمة الإرجاع

أ[`Document`](../../document/) كائن يمثل مستند Word.

## ملاحظات

هذه الطريقة هي نفس استدعاء[`Document`](../../document/) منشئ مع معلمة تدفق.

## أمثلة

يوضح كيفية فتح المستندات باستخدام فئة ComHelper.

```csharp
// تسمح لنا فئة ComHelper بتحميل المستندات من داخل عملاء COM.
ComHelper comHelper = new ComHelper();

// 1 - استخدام اسم ملف النظام المحلي:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - من مجرى:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### أنظر أيضا

* class [Document](../../document/)
* class [ComHelper](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
