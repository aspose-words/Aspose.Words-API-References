---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources метод"
linktitle: "get_ExportCidUrlsForMhtmlResources"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources метод. Указывает, следует ли использовать CID (Content-ID) URL для ссылки на ресурсы (изображения, шрифты, CSS), включённые в документы MHTML. Значение по умолчанию — false в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/get_exportcidurlsformhtmlresources/
---
## HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources method


Указывает, следует ли использовать CID (Content-ID) URL для ссылки на ресурсы (изображения, шрифты, CSS), включённые в документы MHTML. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources() const
```

## Примечания


Эта опция влияет только на документы, сохраняемые в MHTML.

По умолчанию ресурсы в документах MHTML ссылаются по имени файла (например, \"image.png\"), которое сопоставляется с заголовками \"Content-Location\" MIME‑частей.

Эта опция включает альтернативный метод, при котором ссылки на файлы ресурсов записываются как CID (Content-ID) URL (например, \"cid:image.png\") и сопоставляются с заголовками \"Content-ID\".

Теоретически не должно быть разницы между двумя методами ссылки, и любой из них должен работать нормально в любом браузере или почтовом клиенте. На практике же некоторые клиенты не могут получить ресурсы по имени файла. Если ваш браузер или почтовый клиент отказывается загружать ресурсы, включённые в документ MTHML (не отображает изображения или не загружает стили CSS), попробуйте экспортировать документ с CID URL.

## Примеры



Показывает, как включить идентификаторы контента для выходных документов MHTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Установка этого флага заменит теги \"Content-Location\"
// на теги \"Content-ID\" для каждого ресурса из входного документа.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Mhtml);
options->set_ExportCidUrlsForMhtmlResources(exportCidUrlsForMhtmlResources);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-ID: <document.html>"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"Content-Location: document.html"));
    ASSERT_TRUE(outDocContents.Contains(u"<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    ASSERT_TRUE(outDocContents.Contains(u"@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    ASSERT_TRUE(outDocContents.Contains(u"<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

## См. также

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
