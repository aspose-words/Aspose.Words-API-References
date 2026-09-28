---
title: "Метод Aspose::Words::Document::get_OriginalFileName"
linktitle: "get_OriginalFileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::get_OriginalFileName. Получает оригинальное имя файла документа в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words/document/get_originalfilename/
---
## Document::get_OriginalFileName method


Получает исходное имя файла документа.

```cpp
System::String Aspose::Words::Document::get_OriginalFileName() const
```

## Примечания


Возвращает **null**, если документ был загружен из потока или создан пустым.

## Примеры



Показывает, как получить детали операции загрузки документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(get_MyDir() + u"Document.docx", doc->get_OriginalFileName());
ASSERT_EQ(Aspose::Words::LoadFormat::Docx, doc->get_OriginalLoadFormat());
```


Показывает, как использовать методы [FileFormatUtil](../../fileformatutil/) для определения формата документа.
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

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
