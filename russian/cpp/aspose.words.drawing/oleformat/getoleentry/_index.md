---
title: "Метод Aspose::Words::Drawing::OleFormat::GetOleEntry"
linktitle: "GetOleEntry"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::OleFormat::GetOleEntry. Получает запись данных объекта OLE в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.drawing/oleformat/getoleentry/
---
## OleFormat::GetOleEntry method


Получает запись данных OLE-объекта.

```cpp
System::SharedPtr<System::IO::MemoryStream> Aspose::Words::Drawing::OleFormat::GetOleEntry(const System::String &oleEntryName)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| oleEntryName | const System::String\& | Регистрозависимое имя потока данных OLE. |

### ReturnValue

Поток данных OLE или **null**.

## Примеры



Показывает, как вставлять связанные и несвязанные объекты OLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте рисунок Microsoft Visio в документ как объект OLE.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", false, false, nullptr);

// Вставьте ссылку на файл в локальной файловой системе и отобразите её как значок.
builder->InsertOleObject(get_ImageDir() + u"Microsoft Visio drawing.vsd", u"Package", true, true, nullptr);

// Вставка объектов OLE создаёт фигуры, которые хранят эти объекты.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());
ASSERT_EQ(2, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::OleObject;
}))));

// Если фигура содержит объект OLE, у неё будет действительное свойство "OleFormat",
// которое мы можем использовать для проверки некоторых аспектов фигуры.
System::SharedPtr<Aspose::Words::Drawing::OleFormat> oleFormat = shapes[0]->get_OleFormat();

ASPOSE_ASSERT_EQ(false, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(false, oleFormat->get_OleIcon());

oleFormat = shapes[1]->get_OleFormat();

ASPOSE_ASSERT_EQ(true, oleFormat->get_IsLink());
ASPOSE_ASSERT_EQ(true, oleFormat->get_OleIcon());

ASSERT_TRUE(oleFormat->get_SourceFullName().EndsWith(System::String(u"Images") + System::IO::Path::DirectorySeparatorChar + u"Microsoft Visio drawing.vsd"));
ASSERT_EQ(u"", oleFormat->get_SourceItem());

ASSERT_EQ(u"Microsoft Visio drawing.vsd", oleFormat->get_IconCaption());

doc->Save(get_ArtifactsDir() + u"Shape.OleLinks.docx");

// Если объект содержит данные OLE, мы можем получить к ним доступ с помощью потока.
{
    System::SharedPtr<System::IO::MemoryStream> stream = oleFormat->GetOleEntry(u"\x0001" u"CompObj");
    System::ArrayPtr<uint8_t> oleEntryBytes = stream->ToArray();
    ASSERT_EQ(76, oleEntryBytes->get_Length());
}
```

## См. также

* Class [OleFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
