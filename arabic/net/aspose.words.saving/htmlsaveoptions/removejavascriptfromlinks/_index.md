---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words لـ .NET
description: قم بتحسين محتوى الويب الخاص بك باستخدام HtmlSaveOptions لإزالة JavaScript بسهولة من الروابط، مما يؤدي إلى تحسين الأداء وتحسين تجربة المستخدم.
type: docs
weight: 410
url: /ar/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. الافتراضي هو`خطأ شنيع` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## ملاحظات

عند تفعيل هذا الخيار، سيتم استبدال جميع الروابط التي تحتوي على جافا سكريبت (مثل الروابط التي تحتوي على "javascript:" في سمة href) بـ "javascript:void(0)". هذا يُساعد في منع المخاطر الأمنية المحتملة، مثل هجمات XSS.

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
