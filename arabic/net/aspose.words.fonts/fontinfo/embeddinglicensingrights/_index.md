---
title: FontInfo.EmbeddingLicensingRights
linktitle: EmbeddingLicensingRights
articleTitle: EmbeddingLicensingRights
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontInfo EmbeddingLicensingRights للوصول بسهولة إلى حقوق ترخيص الخطوط المضمنة لديك وإدارتها لضمان تكامل التصميم بسلاسة.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontinfo/embeddinglicensingrights/
---
## FontInfo.EmbeddingLicensingRights property

يحصل على حقوق ترخيص الخط المضمن.

```csharp
public FontEmbeddingLicensingRights EmbeddingLicensingRights { get; }
```

## ملاحظات

قد تكون القيمة فارغة إذا لم يتم تضمين الخط.

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

* class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* class [FontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
