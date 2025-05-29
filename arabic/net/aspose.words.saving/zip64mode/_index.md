---
title: Zip64Mode Enum
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.Zip64Mode enum لاستخدام تنسيق ZIP64 بكفاءة في ملفات OOXML، مما يعزز إدارة حجم الملف والتوافق.
type: docs
weight: 6550
url: /ar/net/aspose.words.saving/zip64mode/
---
## Zip64Mode enumeration

يحدد متى يتم استخدام ملحقات تنسيق ZIP64 لملفات OOXML.

```csharp
public enum Zip64Mode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Never | `0` | لا تستخدم امتدادات تنسيق ZIP64. |
| IfNecessary | `1` | إذا لزم الأمر، استخدم امتدادات تنسيق ZIP64. |
| Always | `2` | استخدم دائمًا امتدادات تنسيق ZIP64. |

## ملاحظات

ملف OOXML هو أرشيف ZIP له حد 4 جيجابايت (2 ^ 32 بايت) لحجم الملف غير المضغوط، وحجم الملف المضغوط، والحجم الإجمالي للأرشيف، بالإضافة إلى حد 65535 (2 ^ 16-1) ملف في الأرشيف. تزيد امتدادات تنسيق ZIP64 من الحدود إلى 2 ^ 64.

## أمثلة

يوضح كيفية استخدام ملحقات تنسيق ZIP64.

```csharp
Random random = new Random();
DocumentBuilder builder = new DocumentBuilder();

for (int i = 0; i < 10000; i++)
{
    using (Bitmap bmp = new Bitmap(5, 5))
    using (Graphics g = Graphics.FromImage(bmp))
    {
        g.Clear(Color.FromArgb(random.Next(0, 254), random.Next(0, 254), random.Next(0, 254)));
        using (MemoryStream ms = new MemoryStream())
        {
            bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
            builder.InsertImage(ms.ToArray());
        }
    }
}

builder.Document.Save(ArtifactsDir + "OoxmlSaveOptions.Zip64ModeOption.docx", 
    new OoxmlSaveOptions { Zip64Mode = Zip64Mode.Always });
```

### أنظر أيضا

* property [Zip64Mode](../ooxmlsaveoptions/zip64mode/)
* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
