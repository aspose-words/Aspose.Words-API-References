---
title: PhysicalFontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PhysicalFontInfo EmbeddingLicensingRights—افتح حقوق تضمين الخطوط الأساسية لتحقيق تكامل سلس للتصميم.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/physicalfontinfo/embeddinglicensingrights/
---
## PhysicalFontInfo.EmbeddingLicensingRights property

تضمين حقوق الترخيص للخط.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## أمثلة

يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المضمنة (PhysicalFontInfo).

```csharp
FontSettings settings = FontSettings.DefaultInstance;
FontSourceBase source = settings.GetFontsSources()[0];

// احصل على قائمة الخطوط المتوفرة.
IList<PhysicalFontInfo> fontInfos = source.GetAvailableFonts();
foreach (PhysicalFontInfo fontInfo in fontInfos)
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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [PhysicalFontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
