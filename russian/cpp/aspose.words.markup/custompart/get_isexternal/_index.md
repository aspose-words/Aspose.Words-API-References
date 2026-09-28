---
title: "Метод Aspose::Words::Markup::CustomPart::get_IsExternal"
linktitle: "get_IsExternal"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::CustomPart::get_IsExternal. False, если эта пользовательская часть хранится внутри пакета OOXML. True, если эта пользовательская часть является внешней целью в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.markup/custompart/get_isexternal/
---
## CustomPart::get_IsExternal method


False, если эта пользовательская часть хранится внутри пакета OOXML. True, если эта пользовательская часть является внешней целью.

```cpp
bool Aspose::Words::Markup::CustomPart::get_IsExternal() const
```

## Примечания


Значение по умолчанию — **false**.

## Примеры



Показывает, как получить доступ к коллекции произвольных пользовательских частей документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Клонируйте вторую часть, затем добавьте клон в коллекцию.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Переберите коллекцию и выведите каждую часть.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomPart>>> enumerator = doc->get_PackageCustomParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Part index {0}:", index) << std::endl;
        std::cout << System::String::Format(u"\tName:\t\t\t\t{0}", enumerator->get_Current()->get_Name()) << std::endl;
        std::cout << System::String::Format(u"\tContent type:\t\t{0}", enumerator->get_Current()->get_ContentType()) << std::endl;
        std::cout << System::String::Format(u"\tRelationship type:\t{0}", enumerator->get_Current()->get_RelationshipType()) << std::endl;
        std::cout << (enumerator->get_Current()->get_IsExternal() ? u"\tSourced from outside the document" : System::String::Format(u"\tStored within the document, length: {0} bytes", enumerator->get_Current()->get_Data()->get_Length())) << std::endl;
        index++;
    }
}

// Мы можем удалять элементы из этой коллекции по отдельности или сразу все.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## См. также

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
