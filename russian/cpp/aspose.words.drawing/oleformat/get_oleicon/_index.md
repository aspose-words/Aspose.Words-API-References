---
title: "Метод Aspose::Words::Drawing::OleFormat::get_OleIcon"
linktitle: "get_OleIcon"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::OleFormat::get_OleIcon. Получает аспект отображения объекта OLE. Когда true, объект OLE отображается как значок. Когда false, объект OLE отображается как содержимое в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing/oleformat/get_oleicon/
---
## OleFormat::get_OleIcon method


Получает аспект отображения OLE-объекта. Когда **true**, OLE-объект отображается как значок. Когда **false**, OLE-объект отображается как содержимое.

```cpp
bool Aspose::Words::Drawing::OleFormat::get_OleIcon()
```

## Примечания


Aspose.Words не позволяет устанавливать это свойство, чтобы избежать путаницы. Если бы вы могли изменить аспект отображения в Aspose.Words, Microsoft Word всё равно отображал бы объект OLE в его оригинальном виде, пока вы не отредактируете или не обновите объект OLE в Microsoft Word.

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
