---
title: FontEmbeddingLicensingRights.NoSubsetting
linktitle: NoSubsetting
articleTitle: NoSubsetting
second_title: Aspose.Words لـ .NET
description: اكتشف حقوق ترخيص تضمين الخطوط دون أي تنازلات. اضمن الامتثال واحمِ خطوطك مع تحسين مشاريع التصميم الخاصة بك.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/fontembeddinglicensingrights/nosubsetting/
---
## FontEmbeddingLicensingRights.NoSubsetting property

يشير إلى قيد "عدم التقسيم الفرعي".

```csharp
public bool NoSubsetting { get; }
```

## ملاحظات

عند ضبط هذا العلم، يجب عدم تجزئة الخط قبل التضمين. تنطبق أيضًا قيود تضمين أخرى.

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
