---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words لـ .NET
description: FolderFontSource ScanSubfolders ملكية. تحديد ما إذا كان سيتم فحص المجلدات الفرعية أم لا في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

تحديد ما إذا كان سيتم فحص المجلدات الفرعية أم لا.

```csharp
public bool ScanSubfolders { get; }
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

* class [FolderFontSource](../)
* مساحة الاسم [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../../)
