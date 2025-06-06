---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words لـ .NET
description: تحكم في تصدير اللغة بتنسيق HTML أو MHTML أو EPUB باستخدام خيارات حفظ Html. حسّن إمكانية الوصول إلى المستندات ووسّع نطاق وصولك إلى جمهور أوسع بسهولة.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

يحدد ما إذا كان سيتم تصدير معلومات اللغة إلى HTML أو MHTML أو EPUB. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية على`حقيقي` مخرجات Aspose.Words**اللغة**سمة HTML على عناصر document التي تحدد اللغة. قد يكون هذا ضروريًا للحفاظ على الدلالات المتعلقة باللغة.

## أمثلة

يوضح كيفية الحفاظ على معلومات اللغة عند الحفظ في .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم المنشئ لكتابة النص أثناء تنسيقه في مواقع مختلفة.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// عند حفظ المستند في HTML، يمكننا تمرير كائن SaveOptions
// إما للحفاظ على إعدادات كل نص منسق أو تجاهلها.
// إذا قمنا بتعيين علم "ExportLanguageInformation" إلى "true"،
// ستحتوي وثيقة HTML الناتجة على الإعدادات المحلية في سمات "lang" الخاصة بعلامات <span>.
// إذا قمنا بتعيين علم "ExportLanguageInformation" إلى "false"،
// لن يحتوي النص الموجود في مستند HTML الناتج على أي معلومات محلية.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    Assert.True(outDocContents.Contains("<span>Hello world!</span>"));
    Assert.True(outDocContents.Contains("<span>Hello again!</span>"));
    Assert.True(outDocContents.Contains("<span>Привет, мир!</span>"));
}
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
