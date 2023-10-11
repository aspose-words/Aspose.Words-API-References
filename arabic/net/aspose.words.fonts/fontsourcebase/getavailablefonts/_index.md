---
title: FontSourceBase.GetAvailableFonts
second_title: Aspose.Words لمراجع .NET API
description: FontSourceBase طريقة. إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

إرجاع قائمة الخطوط المتوفرة عبر هذا المصدر.

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* مساحة الاسم [Aspose.Words.Fonts](../../fontsourcebase/)
* المجسم [Aspose.Words](../../../)


