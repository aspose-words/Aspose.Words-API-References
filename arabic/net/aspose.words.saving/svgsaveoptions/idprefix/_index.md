---
title: SvgSaveOptions.IdPrefix
linktitle: IdPrefix
articleTitle: IdPrefix
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية SvgSaveOptions IdPrefix، التي تُخصّص مُعرِّفات العناصر في مستندك المُخرَج لتحسين التنظيم والوضوح. حسّن ملفات SVG الخاصة بك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.saving/svgsaveoptions/idprefix/
---
## SvgSaveOptions.IdPrefix property

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

يوضح كيفية إضافة بادئة مضافة إلى جميع معرفات العناصر المولدة (svg).

```csharp
Document doc = new Document(MyDir + "Id prefix.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.IdPrefix = "pfx1_";

doc.Save(ArtifactsDir + "SvgSaveOptions.IdPrefixSvg.html", saveOptions);
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
