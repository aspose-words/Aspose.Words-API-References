---
title: "Aspose::Words::FileFormatUtil::SaveFormatToExtension метод"
linktitle: "SaveFormatToExtension"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::FileFormatUtil::SaveFormatToExtension метод. Преобразует перечисленное значение формата сохранения в расширение файла. Возвращаемое расширение — строка в нижнем регистре с ведущей точкой в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/fileformatutil/saveformattoextension/
---
## FileFormatUtil::SaveFormatToExtension method


Преобразует перечисляемое значение формата сохранения в расширение файла. Возвращаемое расширение — строка в нижнем регистре с ведущей точкой.

```cpp
static System::String Aspose::Words::FileFormatUtil::SaveFormatToExtension(Aspose::Words::SaveFormat saveFormat)
```

## Примечания


Значение [WordML](../../saveformat/) преобразуется в ".wml".

Значение [FlatOpc](../../saveformat/) преобразуется в ".fopc".

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
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
