---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ConvertSvgToEmf في HtmlLoadOptions. تحكّم بسهولة في تحويل SVG إلى EMF للحصول على جودة صورة مثالية. الوضع الافتراضي هو "خطأ"، لذا حافظ على ملفات SVG سليمة!
type: docs
weight: 30
url: /ar/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان سيتم تحويل صور SVG المحملة إلى تنسيق EMF. القيمة الافتراضية هي`خطأ شنيع` وإذا كان ذلك ممكنًا، يتم تخزين صور SVG المحملة كما هي دون تحويل.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## ملاحظات

تدعم الإصدارات الأحدث من مايكروسوفت وورد صور SVG بشكل أصلي. إذا كان إصدار مايكروسوفت وورد المحدد في خيارات التحميل يدعم صور SVG، فسيخزن Aspose.Words صور SVG كما هي دون تحويل. إذا لم يكن SVG مدعومًا، فسيتم تحويل صور SVG المُحمّلة إلى تنسيق EMF.

ومع ذلك، إذا تم تعيين هذا الخيار على`حقيقي` سيقوم Aspose.Words بتحويل صور SVG المحملة إلى EMF حتى إذا كانت صور SVG مدعومة بواسطة الإصدار المحدد من MS Word.

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

* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
