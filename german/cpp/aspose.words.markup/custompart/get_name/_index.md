---
title: "Aspose::Words::Markup::CustomPart::get_Name-Methode"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomPart::get_Name-Methode. Gibt den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder die Ziel-URL in C++ zurück bzw. setzt ihn."
type: docs
weight: 7000
url: /de/cpp/aspose.words.markup/custompart/get_name/
---
## CustomPart::get_Name method


Liest oder setzt den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder die Ziel-URL.

```cpp
System::String Aspose::Words::Markup::CustomPart::get_Name() const
```

## Hinweise


Wenn das Beziehungsziel intern ist, ist diese Eigenschaft der absolute Teilname innerhalb des Pakets. Wenn das Beziehungsziel extern ist, ist diese Eigenschaft die Ziel-URL.

Der Standardwert ist ein leerer String. Ein gültiger Wert muss ein nicht-leerer String sein.

## Beispiele



Zeigt, wie man auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugreift.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Klonen Sie den zweiten Teil und fügen Sie dann den Klon zur Sammlung hinzu.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Durchlaufen Sie die Sammlung und geben Sie jeden Teil aus.
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

// Wir können Elemente aus dieser Sammlung einzeln oder alle auf einmal entfernen.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Siehe auch

* Class [CustomPart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
