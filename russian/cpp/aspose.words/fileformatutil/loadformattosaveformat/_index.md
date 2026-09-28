---
title: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat метод"
linktitle: "LoadFormatToSaveFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat метод. Преобразует значение LoadFormat в значение SaveFormat, если это возможно, в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/fileformatutil/loadformattosaveformat/
---
## FileFormatUtil::LoadFormatToSaveFormat method


Преобразует значение [LoadFormat](../../loadformat/) в значение [SaveFormat](../../saveformat/), если это возможно.

```cpp
static Aspose::Words::SaveFormat Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(Aspose::Words::LoadFormat loadFormat)
```


## Примеры



Показывает, как использовать методы [FileFormatUtil](../) для определения формата документа.
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

* Enum [SaveFormat](../../saveformat/)
* Enum [LoadFormat](../../loadformat/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
