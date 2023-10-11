---
title: PhysicalFontInfo.FontFamilyName
second_title: Aspose.Words لمراجع .NET API
description: PhysicalFontInfo ملكية. اسم عائلة الخط.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/physicalfontinfo/fontfamilyname/
---
## PhysicalFontInfo.FontFamilyName property

اسم عائلة الخط.

```csharp
public string FontFamilyName { get; }
```

### أمثلة

يوضح كيفية سرد الخطوط المتاحة.

```csharp
// قم بتكوين Aspose.Words لمصدر الخطوط من مجلد مخصص، ثم قم بطباعة كل خط متاح.
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


