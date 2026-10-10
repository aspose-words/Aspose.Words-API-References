---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames"
linktitle: "get_ResolveFontNames"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames. يحدد ما إذا كانت أسماء عائلات الخطوط المستخدمة في المستند يتم حلها واستبدالها وفقًا لـ FontSettings عند كتابتها إلى صيغ تعتمد على HTML في C++."
type: docs
weight: 42000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


يحدد ما إذا كانت أسماء عائلات الخطوط المستخدمة في المستند يتم حلها واستبدالها وفقًا لـ [FontSettings](../../../aspose.words/document/get_fontsettings/) عند كتابتها إلى صيغ تعتمد على HTML.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## ملاحظات


بشكل افتراضي، يتم تعيين هذا الخيار إلى **false** وتُكتب أسماء عائلات الخطوط إلى HTML كما هو محدد في المستندات المصدر. أي أن [FontSettings](../../../aspose.words/document/get_fontsettings/) تُهمل ولا يتم أي حل أو استبدال لأسماء عائلات الخطوط.

إذا تم تعيين هذا الخيار إلى **true**، يستخدم Aspose.Words [FontSettings](../../../aspose.words/document/get_fontsettings/) لحل كل اسم عائلة خط محدد في مستند المصدر إلى اسم عائلة خط متاحة، مع إجراء استبدال الخطوط حسب الحاجة.

## أمثلة



يوضح كيفية حل جميع أسماء الخطوط قبل كتابتها إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// يحتوي هذا المستند على نص يذكر خطًا لا نمتلكه.
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// إذا لم يكن لدينا طريقة للحصول على هذا الخط، وأردنا أن نتمكن من عرض جميع النصوص
// في هذا المستند في ملف HTML الناتج، يمكننا استبداله بخط آخر.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// بشكل افتراضي، يتم تعيين هذا الخيار إلى 'False' وتقوم Aspose.Words بكتابة أسماء الخطوط كما هو محدد في المستند الأصلي
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
