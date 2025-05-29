---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية HtmlSaveOptions ResolveFontNames على تحسين تنسيق المستندات من خلال ضمان استبدال الخطوط بدقة في مخرجات HTML.
type: docs
weight: 430
url: /ar/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

يحدد ما إذا كانت أسماء عائلة الخطوط المستخدمة في المستند يتم حلها واستبدالها وفقًا لـ [`FontSettings`](../../../aspose.words/document/fontsettings/) عند كتابتها بتنسيقات تعتمد على HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## ملاحظات

بشكل افتراضي، يتم تعيين هذا الخيار على`خطأ شنيع` وأسماء عائلات الخطوط مكتوبة في HTML بصيغة specific في المستندات المصدرية. أي،[`FontSettings`](../../../aspose.words/document/fontsettings/) يتم تجاهلها ولا يتم تنفيذ أي حل أو استبدال لأسماء عائلة الخطوط.

إذا تم تعيين هذا الخيار على`حقيقي` ، يستخدم Aspose.Words[`FontSettings`](../../../aspose.words/document/fontsettings/) لحل كل اسم عائلة خط محدد في مستند مصدر إلى اسم عائلة خط متوفرة، وإجراء استبدال الخط حسب الحاجة.

## أمثلة

يوضح كيفية حل جميع أسماء الخطوط قبل كتابتها في HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// تحتوي هذه الوثيقة على نص يسمي خطًا لا نملكه.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// إذا لم يكن لدينا طريقة للحصول على هذا الخط، وأردنا أن نتمكن من عرض النص بأكمله
// في هذه الوثيقة في إخراج HTML، يمكننا استبداله بخط آخر.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // بشكل افتراضي، يتم تعيين هذا الخيار على "False" ويكتب Aspose.Words أسماء الخطوط كما هو محدد في المستند المصدر
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
