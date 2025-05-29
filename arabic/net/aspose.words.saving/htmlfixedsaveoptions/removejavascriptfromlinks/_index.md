---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words لـ .NET
description: حسّن أداء HTML باستخدام ميزة HtmlFixedSaveOptions RemoveJavaScriptFromLinks. حسّن أمان موقعك بإزالة JavaScript من الروابط بسهولة.
type: docs
weight: 140
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. الافتراضي هو`خطأ شنيع` .

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## ملاحظات

عند تفعيل هذا الخيار، سيتم استبدال جميع الروابط التي تحتوي على جافا سكريبت (مثل الروابط التي تحتوي على "javascript:" في سمة href) بـ "javascript:void(0)". هذا يُساعد في منع المخاطر الأمنية المحتملة، مثل هجمات XSS.

## أمثلة

يوضح كيفية إزالة JavaScript من الروابط.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

يوضح كيفية إزالة JavaScript من الروابط الخاصة بالمستندات الثابتة بتنسيق HTML.

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
