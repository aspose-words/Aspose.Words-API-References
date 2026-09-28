---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages метод"
linktitle: "get_ExportEmbeddedImages"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages метод. Указывает, должны ли изображения быть встроены в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/get_exportembeddedimages/
---
## HtmlFixedSaveOptions::get_ExportEmbeddedImages method


Указывает, следует ли внедрять изображения в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html.

```cpp
bool Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages() const
```


## Примеры



Показывает, как определить, где хранить изображения при экспорте документа в Html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Когда мы экспортируем документ с встроенными изображениями в .html,
// Aspose.Words может разместить изображения в двух возможных местах.
// Установка флага "ExportEmbeddedImages" в значение "true" сохранит необработанные данные
// для всех изображений в выходном документе HTML, в атрибуте "src" тегов <image>.
// Установка этого флага в значение "false" создаст файл изображения в локальной файловой системе для каждого изображения,
// и сохранит все эти файлы в отдельной папке.
auto htmlFixedSaveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
htmlFixedSaveOptions->set_ExportEmbeddedImages(exportImages);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />")->get_Success());
}
else
{
    ASSERT_TRUE(System::IO::File::Exists(get_ArtifactsDir() + u"HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" ") + u"src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />")->get_Success());
}
```

## См. также

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
