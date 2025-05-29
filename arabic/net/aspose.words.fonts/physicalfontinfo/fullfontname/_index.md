---
title: PhysicalFontInfo.FullFontName
linktitle: FullFontName
articleTitle: FullFontName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FullFontName في PhysicalFontInfo للوصول بسهولة إلى أسماء الخطوط. حسّن أسلوبك في الطباعة بتحديد دقيق للخطوط!
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/physicalfontinfo/fullfontname/
---
## PhysicalFontInfo.FullFontName property

الاسم الكامل للخط.

```csharp
public string FullFontName { get; }
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
