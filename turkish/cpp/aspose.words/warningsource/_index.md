---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WarningSource enum. C++'da belge yükleme veya kaydetme sırasında uyarı üreten modülü belirtir."
type: docs
weight: 128000
url: /tr/cpp/aspose.words/warningsource/
---
## WarningSource enum


Belge yüklenirken veya kaydedilirken uyarı üreten modülü belirtir.

```cpp
enum class WarningSource
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Bilinmiyor | 0 | Uyarı kaynağı belirtilmemiştir. |
| Düzen | 1 | Belge düzeni oluşturan modül. |
| DrawingML | 2 | DrawingML şekillerini render eden modül. |
| OfficeMath | 3 | OfficeMath'ı render eden modül. |
| Shapes | 4 | Normal şekilleri render eden modül. |
| Metafile | 5 | Metafile'ları render eden modül. |
| Xps | 6 | XPS'yi render eden modül. |
| Pdf | 7 | PDF'yi render eden modül. |
| Image | 8 | Görüntüleri render eden modül. |
| Docx | 9 | DOCX dosyalarını okuyan/yazan modül. |
| Doc | 10 | İkili DOC dosyalarını okuyan/yazan modül. |
| Metin | 11 | Düz metin dosyalarını okuyan/yazan modül. |
| Rtf | 12 | RTF dosyalarını okuyan/yazan modül. |
| WordML | 13 | WML dosyalarını okuyan/yazan modül. |
| Nrx | 14 | DOCX/WML okuma/yazma modülleri arasında paylaşılan ortak modüller. |
| Odt | 15 | ODT dosyalarını okuyan/yazan modül. |
| Html | 16 | HTML/MHTML dosyalarını okuyan/yazan modül. |
| Validator | 17 | Model tutarlılığını ve geçerliliğini doğrulayan modül. |
| Xaml | 18 | Xaml dosyalarını okuyan/yazan modül. |
| Svm | 19 | Svm dosyalarını okuyan modül. |
| MathML | 20 | W3C MathML dosyalarını okuyan modül. |
| Font | 21 | Yazı tipi dosyalarını okuyan modül. |
| Svg | 22 | SVG dosyalarını okuyan modül. |
| Markdown | 23 | Markdown dosyalarını okuyan/yazan modül. |
| Chm | 24 | CHM dosyalarını okuyan modül. |
| Epub | 25 | EPUB dosyalarını okuyan/yazan modül. |
| Xml | 26 | XML dosyalarını okuyan modül. |
| Xlsx | 27 | XLSX dosyalarını yazan modül. |
| Docling | 28 | Docling JSON dosyalarını yazan modül. |


## Örnekler



Uyarı kaynağıyla nasıl çalışılacağını gösterir.
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


Yazı tipi ikamesi hakkında ek bilgi almanın nasıl yapılacağını gösterir.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
