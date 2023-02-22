---
title: PhysicalFontInfo.Version
second_title: Aspose.Words لمراجع .NET API
description: PhysicalFontInfo ملكية. سلسلة إصدار الخط .
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

سلسلة إصدار الخط .

```csharp
public string Version { get; }
```

### أمثلة

يوضح كيفية سرد الخطوط المتاحة.

```csharp
// تكوين Aspose.Words لخطوط المصدر من مجلد مخصص ، ثم طباعة كل خط متاح.
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
* مساحة الاسم [Aspose.Words.Fonts](../../physicalfontinfo/)
* المجسم [Aspose.Words](../../../)


