---
title: PhysicalFontInfo.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PhysicalFontInfo FilePath، وحدد موقع ملفات الخطوط الخاصة بك بسهولة لتحقيق تكامل سلس في التصميم وتحسين الطباعة في مشاريعك.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

المسار إلى ملف الخط إن وجد.

```csharp
public string FilePath { get; }
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
