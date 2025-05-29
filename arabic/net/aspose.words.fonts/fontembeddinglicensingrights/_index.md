---
title: FontEmbeddingLicensingRights Class
linktitle: FontEmbeddingLicensingRights
articleTitle: FontEmbeddingLicensingRights
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Fonts.FontEmbeddingLicensingRights لإدارة حقوق تضمين الخطوط بسهولة وتحسين عرض مستندك.
type: docs
weight: 3310
url: /ar/net/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class

يمثل حقوق الترخيص المضمنة للخط.

```csharp
public class FontEmbeddingLicensingRights
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BitmapEmbeddingOnly](../../aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/) { get; } | يشير إلى قيد "تضمين الخريطة النقطية فقط". |
| [EmbeddingUsagePermissions](../../aspose.words.fonts/fontembeddinglicensingrights/embeddingusagepermissions/) { get; } | أذونات الاستخدام. |
| [NoSubsetting](../../aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/) { get; } | يشير إلى قيد "عدم التقسيم الفرعي". |

## ملاحظات

لمعرفة المزيد، قم بزيارة [قسم مواصفات OpenType](https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fstype) على بوابة Microsoft Typography.

## أمثلة

يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المضمنة (FontInfo).

```csharp
Document doc = new Document(MyDir + "Embedded font rights.docx");

// الحصول على قائمة خطوط المستند.
FontInfoCollection fontInfos = doc.FontInfos;
foreach (FontInfo fontInfo in fontInfos) 
{
    if (fontInfo.EmbeddingLicensingRights != null)
    {
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.EmbeddingUsagePermissions);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.BitmapEmbeddingOnly);
        Console.WriteLine(fontInfo.EmbeddingLicensingRights.NoSubsetting);
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
