---
title: HtmlFixedSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HtmlFixedSaveOptions IdPrefix لتخصيص مُعرِّفات العناصر في مستنداتك. حسّن تنظيمك باستخدام بادئات مُخصصة لنتائج أفضل!
type: docs
weight: 100
url: /ar/net/aspose.words.saving/htmlfixedsaveoptions/idprefix/
---
## HtmlFixedSaveOptions.IdPrefix property

يحدد بادئة يتم إضافتها مسبقًا إلى جميع معرفات العناصر المولدة في المستند الناتج. القيمة الافتراضية هي null ولا يتم إضافة أي بادئة مسبقًا.

```csharp
public string IdPrefix { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentException | القيمة لا تفي بالمتطلبات المحددة أعلاه. |

## ملاحظات

إذا تم تحديد البادئة، فيمكن أن تحتوي فقط على أحرف وأرقام وعلامات سفلية وواصلات، ويجب أن تبدأ بحرف.

## أمثلة

يوضح كيفية إضافة بادئة مضافة إلى جميع معرفات العناصر المولدة.

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.IdPrefix.html", saveOptions);
```

### أنظر أيضا

* class [HtmlFixedSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
