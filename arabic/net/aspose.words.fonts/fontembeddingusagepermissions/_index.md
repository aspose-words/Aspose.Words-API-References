---
title: FontEmbeddingUsagePermissions Enum
linktitle: FontEmbeddingUsagePermissions
articleTitle: FontEmbeddingUsagePermissions
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Fonts.FontEmbeddingUsagePermissions، التي تتيح لك التحكم الدقيق في أذونات تضمين الخطوط لتحسين إدارة المستندات.
type: docs
weight: 3320
url: /ar/net/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enumeration

يمثل أذونات استخدام تضمين الخط.

```csharp
public enum FontEmbeddingUsagePermissions
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Installable | `0` | قد يكون الخط مضمنًا، وقد يتم تثبيته بشكل دائم لاستخدامه على أنظمة بعيدة، أو لاستخدامه بواسطة مستخدمين آخرين. |
| RestrictedLicense | `1` | لا يجوز تعديل الخط أو تضمينه أو استبداله بأي طريقة دون الحصول أولاً على إذن صريح من المالك القانوني. |
| PrintAndPreview | `2` | قد يتم تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى لأغراض عرض المستند أو طباعته. |
| Editable | `3` | قد يتم تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى. |

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
