---
title: "Aspose::Words::LoadFormat enum"
linktitle: "LoadFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::LoadFormat. Указывает формат документа, который будет загружен в C++."
type: docs
weight: 97000
url: /ru/cpp/aspose.words/loadformat/
---
## LoadFormat enum


Указывает формат документа, который будет загружен.

```cpp
enum class LoadFormat
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Авто | 0 | Инструктирует Aspose.Words автоматически определять формат. |
| MsWorks | 8 | Microsoft Works 8 [Документ](../document/). |
| Doc | 10 | Microsoft Word 95 или Word 97 - 2003 [Документ](../document/). |
| Dot | 11 | Шаблон Microsoft Word 95 или Word 97 - 2003. |
| DocPreWord60 | 12 | Документ находится в формате pre-Word 95. В настоящее время Aspose.Words не поддерживает загрузку таких документов. |
| Docx | 20 | Office Open XML WordprocessingML [Документ](../document/) (без макросов). |
| Docm | 21 | Office Open XML WordprocessingML с макросами [Документ](../document/). |
| Dotx | 22 | Шаблон Office Open XML WordprocessingML (без макросов). |
| Dotm | 23 | Шаблон Office Open XML WordprocessingML с макросами. |
| FlatOpc | 24 | Office Open XML WordprocessingML, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcMacroEnabled | 25 | Office Open XML WordprocessingML с макросами [Документ](../document/) хранится в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcTemplate | 26 | Шаблон Office Open XML WordprocessingML (без макросов), хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| FlatOpcTemplateMacroEnabled | 27 | Шаблон Office Open XML WordprocessingML с макросами, хранящийся в плоском XML‑файле вместо ZIP‑пакета. |
| Rtf | 30 | Формат RTF. |
| WordML | 31 | Формат Microsoft Word 2003 WordprocessingML. |
| Html | 50 | Формат HTML. |
| Mhtml | 51 | Формат MHTML (веб-архив). |
| Mobi | 52 | Формат MOBI. Используется в читалках MobiPocket и Amazon Kindle. |
| Chm | 53 | Формат CHM (Compiled HTML Help). |
| Azw3 | 54 | Формат AZW3. Используется в читалках Amazon Kindle. |
| Epub | 55 | Формат EPUB. |
| Odt | 60 | Текст ODF [Document](../document/). |
| Ott | 61 | Шаблон ODF Text [Document](../document/). |
| Text | 62 | Простой текст. |
| Markdown | 63 | Документ в формате Markdown. |
| Xml | 65 | Документ XML. |
| Unknown | 255 | Неопознанный формат, невозможно загрузить с помощью [Aspose.Words](../). |


## Примеры



Показывает, как использовать методы [FileFormatUtil](../fileformatutil/) для определения формата документа.
```cpp
// Загрузите документ из файла без расширения и затем определите его формат.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Ниже представлены два метода преобразования LoadFormat в соответствующий SaveFormat.
    // 1 -  Получите строку расширения файла для LoadFormat, затем получите соответствующий SaveFormat из этой строки:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Преобразуйте LoadFormat напрямую в его SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Загрузите документ из потока и затем сохраните его с автоматически определённым расширением файла.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```


Показывает, как указать базовый URI при открытии HTML‑документа.
```cpp
// Предположим, что мы хотим загрузить .html‑документ, содержащий изображение, связанное относительным URI
// в то время как изображение находится в другом месте. В этом случае нам потребуется преобразовать относительный URI в абсолютный.
// Мы можем задать базовый URI, используя объект HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// Хотя изображение было повреждено во входном .html, наш пользовательский базовый URI помог нам восстановить ссылку.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// Этот выходной документ отобразит отсутствующее изображение.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
