---
title: HtmlSaveOptions.ExportLanguageInformation
second_title: Aspose.Words لمراجع .NET API
description: HtmlSaveOptions ملكية. يحدد ما إذا كان سيتم تصدير معلومات اللغة إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هوخطأ شنيع .
type: docs
weight: 180
url: /ar/net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

يحدد ما إذا كان سيتم تصدير معلومات اللغة إلى HTML أو MHTML أو EPUB. الإعداد الافتراضي هو`خطأ شنيع` .

```csharp
public bool ExportLanguageInformation { get; set; }
```

### ملاحظات

عندما يتم تعيين هذه الخاصية إلى`حقيقي` Aspose.Words النواتج **لانج** سمة HTML في عناصر document التي تحدد اللغة. قد يكون هذا ضروريًا للحفاظ على الدلالات المتعلقة باللغة.

### أمثلة

يوضح كيفية الحفاظ على معلومات اللغة عند الحفظ إلى .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم المنشئ لكتابة النص أثناء تنسيقه في مناطق مختلفة.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// عند حفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions
// إما للحفاظ على لغة كل نص منسق أو تجاهلها.
// إذا قمنا بتعيين علامة "ExportLanguageInformation" على "صحيح"،
// سيحتوي مستند HTML الناتج على الإعدادات المحلية في سمات "lang" الخاصة بـ <span> العلامات.
// إذا قمنا بتعيين علامة "ExportLanguageInformation" على "خطأ"،
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
* مساحة الاسم [Aspose.Words.Saving](../../htmlsaveoptions/)
* المجسم [Aspose.Words](../../../)


