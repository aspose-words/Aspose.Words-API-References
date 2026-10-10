---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::WarningSource enum. يحدد الوحدة التي تُنتج تحذيرًا أثناء تحميل أو حفظ المستند في C++."
type: docs
weight: 128000
url: /ar/cpp/aspose.words/warningsource/
---
## WarningSource enum


يحدد الوحدة التي تُصدر تحذيرًا أثناء تحميل المستند أو حفظه.

```cpp
enum class WarningSource
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| غير معروف | 0 | لم يتم تحديد مصدر التحذير. |
| تخطيط | 1 | الوحدة التي تُنشئ تخطيط المستند. |
| DrawingML | 2 | وحدة تقوم بعرض أشكال DrawingML. |
| OfficeMath | 3 | وحدة تقوم بعرض OfficeMath. |
| الأشكال | 4 | وحدة تقوم بعرض الأشكال العادية. |
| Metafile | 5 | وحدة تقوم بعرض metafiles. |
| Xps | 6 | وحدة تقوم بعرض XPS. |
| Pdf | 7 | وحدة تقوم بعرض PDF. |
| Image | 8 | وحدة تقوم بعرض الصور. |
| Docx | 9 | وحدة تقرأ/تكتب ملفات DOCX. |
| Doc | 10 | وحدة تقرأ/تكتب ملفات DOC الثنائية. |
| Text | 11 | وحدة تقرأ/تكتب ملفات النص العادي. |
| Rtf | 12 | وحدة تقرأ/تكتب ملفات RTF. |
| WordML | 13 | وحدة تقرأ/تكتب ملفات WML. |
| Nrx | 14 | الوحدات المشتركة التي يتم مشاركتها بين وحدات القارئ/الكاتب DOCX/WML. |
| Odt | 15 | وحدة تقرأ/تكتب ملفات ODT. |
| Html | 16 | وحدة تقرأ/تكتب ملفات HTML/MHTML. |
| المتحقق | 17 | الوحدة التي تتحقق من اتساق النموذج وصحته. |
| Xaml | 18 | الوحدة التي تقرأ/تكتب ملفات Xaml. |
| Svm | 19 | الوحدة التي تقرأ ملفات Svm. |
| MathML | 20 | الوحدة التي تقرأ ملفات W3C MathML. |
| Font | 21 | الوحدة التي تقرأ ملفات الخط. |
| Svg | 22 | الوحدة التي تقرأ ملفات SVG. |
| Markdown | 23 | الوحدة التي تقرأ/تكتب ملفات Markdown. |
| Chm | 24 | الوحدة التي تقرأ ملفات CHM. |
| Epub | 25 | الوحدة التي تقرأ/تكتب ملفات EPUB. |
| Xml | 26 | الوحدة التي تقرأ ملفات XML. |
| Xlsx | 27 | الوحدة التي تكتب ملفات XLSX. |
| Docling | 28 | الوحدة التي تكتب ملفات Docling JSON. |


## أمثلة



يعرض كيفية العمل مع مصدر التحذير.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Emphases markdown warning.docx");

auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warnings);
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.EmphasesWarningSourceMarkdown.md");

for (auto&& warningInfo : warnings)
{
    if (warningInfo->get_Source() == Aspose::Words::WarningSource::Markdown)
    {
        ASSERT_EQ(u"The (*, 0:11) cannot be properly written into Markdown.", warningInfo->get_Description());
    }
}
```


يوضح كيفية الحصول على معلومات إضافية حول استبدال الخط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
