---
title: HtmlSaveOptions.MetafileFormat
linktitle: MetafileFormat
articleTitle: MetafileFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MetafileFormat في HtmlSaveOptions للتصدير إلى HTML أو MHTML أو EPUB. احفظ ملفات التعريف كصور PNG عالية الجودة افتراضيًا!
type: docs
weight: 380
url: /ar/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

يحدد التنسيق الذي يتم به حفظ ملفات التعريف عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هيPng ، مما يعني أن الملفات التعريفية يتم تقديمها إلى صور PNG النقطية.

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

## ملاحظات

لا تُعرض ملفات التعريف تلقائيًا بواسطة متصفحات HTML. افتراضيًا، يُحوّل Aspose.Words صور WMF وEMF إلى ملفات PNG عند تصديرها إلى HTML. تتوفر خيارات أخرى لتحويل ملفات التعريف إلى صور SVG أو تصديرها كما هي دون تحويل.

لن يتم تطبيق بعض تحويلات الصور، وخاصة اقتصاص الصور، على صور الملف التعريفي إذا تم تصديرها إلى HTML دون تحويل.

## أمثلة

يوضح كيفية تحويل كائنات SVG إلى تنسيق مختلف عند حفظ مستندات HTML.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' العرض='500' الارتفاع='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// استخدم 'ConvertSvgToEmf' لإرجاع السلوك القديم
// حيث تم تحويل جميع صور SVG المحملة من مستند HTML إلى EMF.
// الآن يتم تحميل صور SVG بدون تحويل
// إذا كان إصدار MS Word المحدد في خيارات التحميل يدعم صور SVG بشكل أصلي.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// تحتوي هذه الوثيقة على عنصر <svg> في شكل نص.
// عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// لتحديد كيفية تعامل عملية الحفظ مع هذا الكائن.
// تعيين خاصية "MetafileFormat" إلى "HtmlMetafileFormat.Png" لتحويلها إلى صورة PNG.
// يؤدي تعيين خاصية "MetafileFormat" إلى "HtmlMetafileFormat.Svg" إلى الحفاظ عليها ككائن SVG.
// تعيين خاصية "MetafileFormat" إلى "HtmlMetafileFormat.EmfOrWmf" لتحويلها إلى ملف تعريفي.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### أنظر أيضا

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
