---
title: "Метод Aspose::Words::Drawing::OlePackage::get_FileName"
linktitle: "get_FileName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::OlePackage::get_FileName. Получает или задает имя файла OLE Package в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/olepackage/get_filename/
---
## OlePackage::get_FileName method


Получает или задает имя файла OLE Package.

```cpp
System::String Aspose::Words::Drawing::OlePackage::get_FileName() const
```


## Примеры



Показывает, как вставить OLE-объект в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// OLE-объекты позволяют открывать другие файлы в локальной файловой системе с помощью другого установленного приложения
// в нашей операционной системе, двойным щелчком по фигуре, содержащей OLE-объект, в теле документа.
// В этом случае наш внешний файл будет ZIP-архивом.
System::ArrayPtr<uint8_t> zipFileBytes = System::IO::File::ReadAllBytes(get_DatabaseDir() + u"cat001.zip");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(zipFileBytes);
    System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertOleObject(stream, u"Package", true, nullptr);

    shape->get_OleFormat()->get_OlePackage()->set_FileName(u"Package file name.zip");
    shape->get_OleFormat()->get_OlePackage()->set_DisplayName(u"Package display name.zip");
}

doc->Save(get_ArtifactsDir() + u"Shape.InsertOlePackage.docx");
```

## См. также

* Class [OlePackage](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
