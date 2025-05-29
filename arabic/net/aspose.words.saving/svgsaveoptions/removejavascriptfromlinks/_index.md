---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words لـ .NET
description: حسّن ملفات SVG باستخدام SvgSaveOptions، واحذف جافا سكريبت بسهولة من الروابط للحصول على كود أكثر وضوحًا. حسّن الأداء والأمان بهذا الإعداد البسيط!
type: docs
weight: 60
url: /ar/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

يحدد ما إذا كان سيتم إزالة JavaScript من الروابط. الافتراضي هو`خطأ شنيع` . إذا تم تمكين هذا الخيار، سيتم استبدال جميع الروابط التي تحتوي على JavaScript بـ "javascript:void(0)".

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## أمثلة

يوضح كيفية إزالة JavaScript من الروابط (svg).

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
