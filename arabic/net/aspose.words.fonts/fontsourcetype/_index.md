---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Fonts.FontSourceType enum لإدارة مصادر الخطوط بكفاءة. حسّن معالجة مستنداتك مع خيارات خطوط مرنة.
type: docs
weight: 3420
url: /ar/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

يحدد نوع مصدر الخط.

```csharp
public enum FontSourceType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| FontFile | `0` | أ[`FileFontSource`](../filefontsource/) كائن يمثل ملف خط واحد. |
| FontsFolder | `1` | أ[`FolderFontSource`](../folderfontsource/) الكائن الذي يمثل المجلد الذي يحتوي على ملفات الخطوط. |
| MemoryFont | `2` | أ[`MemoryFontSource`](../memoryfontsource/) كائن يمثل خطًا واحدًا في الذاكرة. |
| SystemFonts | `3` | أ[`SystemFontSource`](../systemfontsource/) الكائن الذي يمثل جميع الخطوط المثبتة على النظام. |
| FontStream | `4` | أ[`StreamFontSource`](../streamfontsource/) كائن يمثل مجرى بيانات الخط. |

## أمثلة

يوضح كيفية استخدام ملف الخط في نظام الملفات المحلي كمصدر للخط.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fonts](../../aspose.words.fonts/)
* المجسم [Aspose.Words](../../)
