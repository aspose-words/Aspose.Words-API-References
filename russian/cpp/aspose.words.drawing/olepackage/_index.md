---
title: "Класс Aspose::Words::Drawing::OlePackage"
linktitle: "OlePackage"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::OlePackage. Позволяет получать доступ к свойствам OLE Package. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.drawing/olepackage/
---
## OlePackage class


Позволяет получить доступ к свойствам OLE‑Package. Чтобы узнать больше, посетите статью документации [Working with Ole Objects](https://docs.aspose.com/words/cpp/working-with-ole-objects/) .

```cpp
class OlePackage : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayName](./get_displayname/)() const | Получает или задаёт отображаемое имя OLE Package. |
| [get_FileName](./get_filename/)() const | Получает или задает имя файла OLE Package. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayName](./set_displayname/)(System::String) | Сеттер для [Aspose::Words::Drawing::OlePackage::get_DisplayName](./get_displayname/). |
| [set_FileName](./set_filename/)(System::String) | Сеттер для [Aspose::Words::Drawing::OlePackage::get_FileName](./get_filename/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
