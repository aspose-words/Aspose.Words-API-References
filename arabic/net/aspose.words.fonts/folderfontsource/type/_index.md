---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: FolderFontSource Type ملكية. إرجاع نوع مصدر الخط في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

إرجاع نوع مصدر الخط.

```csharp
public override FontSourceType Type { get; }
```

## أمثلة

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
