---
title: OoxmlSaveOptions.Zip64Mode
linktitle: Zip64Mode
articleTitle: Zip64Mode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OoxmlSaveOptions Zip64Mode لتحسين إخراج مستندك بتنسيق ZIP64. حسّن حجم الملفات الكبيرة بسهولة!
type: docs
weight: 80
url: /ar/net/aspose.words.saving/ooxmlsaveoptions/zip64mode/
---
## OoxmlSaveOptions.Zip64Mode property

يحدد ما إذا كان سيتم استخدام امتدادات تنسيق ZIP64 للمستند الناتج أم لا. القيمة الافتراضية هيNever .

```csharp
public Zip64Mode Zip64Mode { get; set; }
```

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

* enum [Zip64Mode](../../zip64mode/)
* class [OoxmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
