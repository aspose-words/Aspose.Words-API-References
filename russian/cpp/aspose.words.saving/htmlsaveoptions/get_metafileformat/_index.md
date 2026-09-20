---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat метод"
linktitle: "get_MetafileFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat метод. Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — Png, что означает, что метафайлы преобразуются в растровые PNG‑изображения в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_metafileformat/
---
## HtmlSaveOptions::get_MetafileFormat method


Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — [Png](../../htmlmetafileformat/), что означает, что метафайлы преобразуются в растровые PNG‑изображения.

```cpp
Aspose::Words::Saving::HtmlMetafileFormat Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat() const
```

## Примечания


Метафайлы не отображаются нативно в браузерах HTML. По умолчанию Aspose.Words преобразует изображения WMF и EMF в файлы PNG при экспорте в HTML. Другие варианты — преобразовать метафайлы в изображения SVG или экспортировать их без конвертации.

Некоторые преобразования изображений, в частности обрезка, не будут применяться к метафайлам, если они экспортируются в HTML без конвертации.

## Примеры



Показывает, как конвертировать SVG‑объекты в другой формат при сохранении HTML‑документов.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Используйте 'ConvertSvgToEmf', чтобы вернуть прежнее поведение
// где все SVG‑изображения, загруженные из HTML‑документа, конвертировались в EMF.
// Теперь SVG‑изображения загружаются без конвертации
// если версия MS Word, указанная в параметрах загрузки, поддерживает SVG‑изображения нативно.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Этот документ содержит элемент <svg> в виде текста.
// При сохранении документа в HTML мы можем передать объект SaveOptions
// чтобы определить, как операция сохранения обрабатывает этот объект.
// Установка свойства "MetafileFormat" в значение "HtmlMetafileFormat.Png" для преобразования его в PNG‑изображение.
// Установка свойства "MetafileFormat" в значение "HtmlMetafileFormat.Svg" сохраняет его как объект SVG.
// Установка свойства "MetafileFormat" в значение "HtmlMetafileFormat.EmfOrWmf" для преобразования его в метафайл.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## См. также

* Enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
