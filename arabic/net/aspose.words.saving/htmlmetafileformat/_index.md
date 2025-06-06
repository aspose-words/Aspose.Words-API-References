---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Saving.HtmlMetafileFormat enum لحفظ ملفات التعريف بسلاسة في مستندات HTML. حسّن تجربة تحويل مستنداتك اليوم!
type: docs
weight: 5840
url: /ar/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

يشير إلى التنسيق الذي يتم به حفظ الملفات التعريفية في مستندات HTML.

```csharp
public enum HtmlMetafileFormat
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Png | `0` | يتم تحويل ملفات التعريف إلى صور PNG نقطية. |
| Svg | `1` | يتم تحويل ملفات التعريف إلى صور SVG متجهة. |
| EmfOrWmf | `2` | يتم حفظ ملفات التعريف كما هي، دون تحويل. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
