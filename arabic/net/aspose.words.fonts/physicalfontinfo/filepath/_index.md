---
title: PhysicalFontInfo.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words لـ .NET
description: PhysicalFontInfo FilePath ملكية. المسار إلى ملف الخط إن وجد في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

المسار إلى ملف الخط إن وجد.

```csharp
public string FilePath { get; }
```

## أمثلة

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
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
