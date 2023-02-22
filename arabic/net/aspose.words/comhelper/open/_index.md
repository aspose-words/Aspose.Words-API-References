---
title: ComHelper.Open
second_title: Aspose.Words لمراجع .NET API
description: ComHelper طريقة. يسمح لتطبيق COM بتحميل ملفDocument من ملف .
type: docs
weight: 20
url: /ar/net/aspose.words/comhelper/open/
---
## Open(string) {#open_1}

يسمح لتطبيق COM بتحميل ملف[`Document`](../../document/) من ملف .

```csharp
public Document Open(string fileName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| fileName | String | اسم ملف المستند المراد تحميله. |

### قيمة الإرجاع

أ[`Document`](../../document/) الذي يمثل مستند Word.

### ملاحظات

هذه الطريقة مماثلة لاستدعاء[`Document`](../../document/) مُنشئ مع معلمة اسم ملف.

### أمثلة

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

// 1 - استخدام اسم ملف نظام محلي:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - من تيار:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### أنظر أيضا

* class [Document](../../document/)
* class [ComHelper](../)
* مساحة الاسم [Aspose.Words](../../comhelper/)
* المجسم [Aspose.Words](../../../)

---

## Open(Stream) {#open}

يسمح بتحميل تطبيق COM[`Document`](../../document/) من تيار .

```csharp
public Document Open(Stream stream)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| stream | Stream | كائن دفق .NET يحتوي على المستند المراد تحميله. |

### قيمة الإرجاع

أ[`Document`](../../document/) الذي يمثل مستند Word.

### ملاحظات

هذه الطريقة مماثلة لاستدعاء[`Document`](../../document/) مُنشئ مع معلمة دفق.

### أمثلة

يوضح كيفية فتح المستندات باستخدام فئة ComHelper.

```csharp
// تسمح لنا فئة ComHelper بتحميل المستندات من داخل عملاء COM.
ComHelper comHelper = new ComHelper();

// 1 - استخدام اسم ملف نظام محلي:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - من تيار:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### أنظر أيضا

* class [Document](../../document/)
* class [ComHelper](../)
* مساحة الاسم [Aspose.Words](../../comhelper/)
* المجسم [Aspose.Words](../../../)


