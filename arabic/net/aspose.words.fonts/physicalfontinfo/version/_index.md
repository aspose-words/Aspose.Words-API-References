---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية إصدار PhysicalFontInfo، وتمكن من الوصول بسهولة إلى سلسلة إصدار الخط لتحسين الاتساق في التصميم وتحسين الطباعة.
type: docs
weight: 50
url: /ar/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

سلسلة إصدار الخط.

```csharp
public string Version { get; }
```

## أمثلة

يوضح كيفية إدراج الخطوط المتوفرة.

```csharp
// قم بتكوين Aspose.Words للحصول على الخطوط من مجلد مخصص، ثم قم بطباعة كل الخطوط المتوفرة.
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### أنظر أيضا

* class [PhysicalFontInfo](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
