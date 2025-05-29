---
title: FontEmbeddingLicensingRights.BitmapEmbeddingOnly
linktitle: BitmapEmbeddingOnly
articleTitle: BitmapEmbeddingOnly
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FontEmbeddingLicensingRights BitmapEmbeddingOnly، التي تضمن قيود تضمين Bitmap الحصرية لتحسين التحكم في التصميم.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/fontembeddinglicensingrights/bitmapembeddingonly/
---
## FontEmbeddingLicensingRights.BitmapEmbeddingOnly property

يشير إلى قيد "تضمين الخريطة النقطية فقط".

```csharp
public bool BitmapEmbeddingOnly { get; }
```

## ملاحظات

عند ضبط هذا البت، يُسمح فقط بتضمين خرائط البت الموجودة في الخط. لا يُسمح بتضمين أي بيانات تفصيلية. إذا لم تتوفر خرائط بت في الخط، يُعتبر الخط غير قابل للتضمين، وستفشل خدمات التضمين. تُطبق أيضًا قيود تضمين أخرى.

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

* class [FontEmbeddingLicensingRights](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
