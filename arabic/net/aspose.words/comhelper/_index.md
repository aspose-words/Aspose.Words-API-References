---
title: Class ComHelper
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.ComHelper فصل. يوفر أساليب لعملاء COM لتحميل مستند إلى Aspose.Words.
type: docs
weight: 220
url: /ar/net/aspose.words/comhelper/
---
## ComHelper class

يوفر أساليب لعملاء COM لتحميل مستند إلى Aspose.Words.

```csharp
public class ComHelper
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [ComHelper](comhelper/)() | تهيئة مثيل جديد لهذه الفئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(Stream) | يسمح بتحميل تطبيق COM[`Document`](../document/) من تيار. |
| [Open](../../aspose.words/comhelper/open/#open_1)(string) | يسمح لتطبيق COM بتحميل ملف[`Document`](../document/) من ملف. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(IStream) | يسمح لتطبيق COM بتحميل ملف[`Document`](../document/) من كائن IStream. |

### ملاحظات

استخدم ال`ComHelper` فئة لتحميل مستند من ملف أو دفق إلى [`Document`](../document/) كائن في تطبيق COM.

ال[`Document`](../document/) توفر الفئة مُنشئًا افتراضيًا لإنشاء مستند جديد وتوفر أيضًا مُنشئات مثقلة لتحميل مستند من ملف أو دفق. إذا كنت تستخدم Aspose.Words من تطبيق .NET، فيمكنك استخدام كافة الميزات[`Document`](../document/) مُنشئات مباشرة، ولكن إذا كنت تستخدم Aspose.Words من تطبيق COM، فإن هو الإعداد الافتراضي فقط[`Document`](../document/) المنشئ متاح.

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

// 1 - استخدام اسم ملف النظام المحلي:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - من الدفق:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


