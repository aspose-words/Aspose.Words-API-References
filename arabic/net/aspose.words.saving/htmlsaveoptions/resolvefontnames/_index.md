---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: Aspose.Words لـ .NET
description: HtmlSaveOptions ResolveFontNames ملكية. يحدد ما إذا كان سيتم حل أسماء مجموعة الخطوط المستخدمة في المستند واستبدالها وفقًا لـ FontSettings عند كتابتها بتنسيقات مستندة إلى HTML في C#.
type: docs
weight: 410
url: /ar/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

يحدد ما إذا كان سيتم حل أسماء مجموعة الخطوط المستخدمة في المستند واستبدالها وفقًا لـ [`FontSettings`](../../../aspose.words/document/fontsettings/) عند كتابتها بتنسيقات مستندة إلى HTML.

```csharp
public bool ResolveFontNames { get; set; }
```

## ملاحظات

افتراضيًا، يتم تعيين هذا الخيار على`خطأ شنيع` وتتم كتابة أسماء عائلة الخطوط إلى HTML كما هو محدد في المستندات المصدر. إنه،[`FontSettings`](../../../aspose.words/document/fontsettings/) يتم تجاهلها ولا يتم تنفيذ أي تحليل أو استبدال لأسماء عائلة الخطوط.

إذا تم ضبط هذا الخيار على`حقيقي` ، يستخدم Aspose.Words[`FontSettings`](../../../aspose.words/document/fontsettings/) لتحويل كل اسم عائلة خطوط محدد في مستند مصدر إلى اسم عائلة خطوط متاحة، وإجراء استبدال الخط كما هو مطلوب.

## أمثلة

يوضح كيفية حل جميع أسماء الخطوط قبل كتابتها إلى HTML.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// يحتوي هذا المستند على نص يُسمي خطًا ليس لدينا.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// إذا لم يكن لدينا طريقة للحصول على هذا الخط، ونريد أن نكون قادرين على عرض النص بأكمله
// في هذا المستند في ملف HTML الناتج، يمكننا استبداله بخط آخر.
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
    // افتراضيًا، يتم تعيين هذا الخيار على "False" ويقوم Aspose.Words بكتابة أسماء الخطوط كما هو محدد في المستند المصدر
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
