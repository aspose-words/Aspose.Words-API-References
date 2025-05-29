---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ScanSubfolders في FolderFontSource لإدارة تنظيم الخطوط بسهولة عن طريق اختيار مسح المجلدات الفرعية لتحسين الكفاءة.
type: docs
weight: 30
url: /ar/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

يحدد ما إذا كان سيتم مسح المجلدات الفرعية أم لا.

```csharp
public bool ScanSubfolders { get; }
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
