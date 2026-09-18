---
title: "Aspose::Words::Document::get_PackageCustomParts Methode"
linktitle: "get_PackageCustomParts"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_PackageCustomParts Methode. Ruft die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) ab oder legt sie fest, die über \"unknown relationships\" mit dem OOXML-Paket in C++ verknüpft sind."
type: docs
weight: 42000
url: /de/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


Liest oder legt die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) fest, die über \"unknown relationships\" mit dem OOXML-Paket verknüpft sind.

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## Hinweise


Verwechseln Sie diese benutzerdefinierten Teile nicht mit Custom XML Data. Wenn Sie auf Custom XML‑Teile zugreifen müssen, verwenden Sie die [CustomXmlParts](../get_customxmlparts/) Eigenschaft.

Diese Sammlung enthält OOXML‑Teile, deren übergeordnetes Element das OOXML‑Paket ist und deren Ziel eine "unknown relationship" darstellt. Weitere Informationen finden Sie unter [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words lädt und speichert benutzerdefinierte Teile ausschließlich in OOXML‑Dokumenten.

Diese Eigenschaft kann nicht **null** sein.

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

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
