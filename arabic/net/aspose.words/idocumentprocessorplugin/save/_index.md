---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words لـ .NET
description: احفظ المستندات بسهولة باستخدام طريقة الحفظ الخاصة بـ IDocumentProcessorPlugin، مما يضمن الحصول على إخراج مثالي مع خيارات الحفظ القابلة للتخصيص وفقًا لاحتياجاتك.
type: docs
weight: 30
url: /ar/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

احفظ المستند المحمل بواسطة[`Load`](../load/) الطريقة إلى مجرى الإخراج باستخدام خيارات الحفظ المحددة.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| outputStream | Stream | تيار الإخراج. |
| saveOptions | SaveOptions | خيارات الحفظ. |

## ملاحظات

إذا كان تنسيق الإخراج المحدد هو صورة، فسيتم حفظ صورة الصفحة الأولى فقط في مجرى الإخراج. إذا لم يكن تنسيق الحفظ المحدد مدعومًا بشكل أصلي بواسطة البرنامج المساعد (يتطلب التحميل إلى[`Document`](../../document/)), الطريقة تطرح استثناءً.

### أنظر أيضا

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
