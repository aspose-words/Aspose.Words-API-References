---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FolderFontSource FolderPath للوصول بسهولة إلى مجلد الخطوط. بسّط سير عملك في التصميم اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

المسار إلى المجلد.

```csharp
public string FolderPath { get; }
```

## أمثلة

يوضح كيفية استخدام مجلد النظام المحلي الذي يحتوي على الخطوط كمصدر للخطوط.

```csharp
// قم بإنشاء مصدر الخط من مجلد يحتوي على ملفات الخطوط.
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
