---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ FolderFontSource لإدارة خطوط سلسة. حسّن مشاريعك على الويب اليوم من خلال مصادر خطوط فعّالة!
type: docs
weight: 10
url: /ar/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

المولد.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| folderPath | String | المسار إلى المجلد. |
| scanSubfolders | Boolean | يحدد ما إذا كان سيتم مسح المجلدات الفرعية أم لا. |

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

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

المولد.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| folderPath | String | المسار إلى المجلد. |
| scanSubfolders | Boolean | يحدد ما إذا كان سيتم مسح المجلدات الفرعية أم لا. |
| priority | Int32 | أولوية مصدر الخط. انظر[`Priority`](../../fontsourcebase/priority/) وصف العقار لمزيد من المعلومات. |

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
