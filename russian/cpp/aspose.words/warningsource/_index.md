---
title: "Aspose::Words::WarningSource enum"
linktitle: "WarningSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WarningSource enum. Указывает модуль, который генерирует предупреждение при загрузке или сохранении документа в C++."
type: docs
weight: 128000
url: /ru/cpp/aspose.words/warningsource/
---
## WarningSource enum


Указывает модуль, который генерирует предупреждение при загрузке или сохранении документа.

```cpp
enum class WarningSource
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Неизвестно | 0 | Источник предупреждения не указан. |
| Макет | 1 | Модуль, который формирует макет документа. |
| DrawingML | 2 | Модуль, который отображает фигуры DrawingML. |
| OfficeMath | 3 | Модуль, который отображает OfficeMath. |
| Shapes | 4 | Модуль, который отображает обычные фигуры. |
| Metafile | 5 | Модуль, который отображает метафайлы. |
| Xps | 6 | Модуль, который отображает XPS. |
| Pdf | 7 | Модуль, который отображает PDF. |
| Image | 8 | Модуль, который отображает изображения. |
| Docx | 9 | Модуль, который читает/записывает файлы DOCX. |
| Doc | 10 | Модуль, который читает/записывает двоичные файлы DOC. |
| Text | 11 | Модуль, который читает/записывает обычные текстовые файлы. |
| Rtf | 12 | Модуль, который читает/записывает файлы RTF. |
| WordML | 13 | Модуль, который читает/записывает файлы WML. |
| Nrx | 14 | Общие модули, которые используются совместно между модулями чтения/записи DOCX и WML. |
| Odt | 15 | Модуль, который читает/записывает файлы ODT. |
| Html | 16 | Модуль, который читает/записывает файлы HTML/MHTML. |
| Validator | 17 | Модуль, проверяющий согласованность и корректность модели. |
| Xaml | 18 | Модуль, читающий/записывающий файлы Xaml. |
| Svm | 19 | Модуль, читающий файлы Svm. |
| MathML | 20 | Модуль, читающий файлы W3C MathML. |
| Font | 21 | Модуль, читающий файлы шрифтов. |
| Svg | 22 | Модуль, читающий файлы SVG. |
| Markdown | 23 | Модуль, читающий/записывающий файлы Markdown. |
| Chm | 24 | Модуль, читающий файлы CHM. |
| Epub | 25 | Модуль, читающий/записывающий файлы EPUB. |
| Xml | 26 | Модуль, читающий файлы XML. |
| Xlsx | 27 | Модуль, записывающий файлы XLSX. |
| Docling | 28 | Модуль, записывающий файлы Docling JSON. |


## Примеры



Показывает, как работать с источником предупреждений.
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


Показывает, как получить дополнительную информацию о замене шрифта.
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

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
