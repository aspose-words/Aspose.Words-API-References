---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words لـ .NET
description: تكامل سلس للمستندات مع Aspose.Words.ComHelper. حمّل وأدر مستنداتك بسهولة لعملاء COM بفضل ميزاته الفعّالة.
type: docs
weight: 410
url: /ar/net/aspose.words/comhelper/
---
## ComHelper class

توفر طرقًا لعملاء COM لتحميل مستند في Aspose.Words.

```csharp
public class ComHelper
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ComHelper](comhelper/)() | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | يسمح لتطبيق COM بالتحميل[`Document`](../document/) من مجرى. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | يسمح لتطبيق COM بتحميل[`Document`](../document/) من ملف. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | يسمح لتطبيق COM بتحميل[`Document`](../document/) من كائن IStream. |

## ملاحظات

استخدم`ComHelper` فئة لتحميل مستند من ملف أو مجرى إلى [`Document`](../document/) كائن في تطبيق COM.

ال[`Document`](../document/) توفر الفئة منشئًا افتراضيًا لإنشاء مستند جديد وتوفر أيضًا منشئين محملين لتحميل مستند من ملف أو مجرى. إذا كنت تستخدم Aspose.Words من تطبيق .NET، فيمكنك استخدام جميع[`Document`](../document/) منشئي مباشرة، ولكن إذا كنت تستخدم Aspose.Words من تطبيق COM، فإن هو الافتراضي فقط[`Document`](../document/) المنشئ متاح.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
