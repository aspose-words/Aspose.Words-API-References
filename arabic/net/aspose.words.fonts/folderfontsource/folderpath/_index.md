---
title: FolderFontSource.FolderPath
second_title: Aspose.Words لمراجع .NET API
description: FolderFontSource ملكية. المسار إلى المجلد.
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

المسار إلى المجلد.

```csharp
public string FolderPath { get; }
```

### أمثلة

يوضح كيفية استخدام مجلد النظام المحلي الذي يحتوي على الخطوط كمصدر للخط.

```csharp
// قم بإنشاء مصدر خط من مجلد يحتوي على ملفات الخطوط.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### أنظر أيضا

* class [FolderFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../folderfontsource/)
* المجسم [Aspose.Words](../../../)


