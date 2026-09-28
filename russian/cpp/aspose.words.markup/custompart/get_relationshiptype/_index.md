---
title: "Aspose::Words::Markup::CustomPart::get_RelationshipType метод"
linktitle: "get_RelationshipType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::CustomPart::get_RelationshipType метод. Получает или задает тип отношения от родительской части к этой пользовательской части в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.markup/custompart/get_relationshiptype/
---
## CustomPart::get_RelationshipType method


Получает или задает тип отношения от родительской части к этой пользовательской части.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_RelationshipType() const
```

## Примечания


Тип отношения для пользовательской части должен быть "unknown" например пользовательский тип отношения, а не один из типов отношений, определённых в ISO/IEC 29500.

Значение по умолчанию — пустая строка. Допустимое значение должно быть непустой строкой.

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
