---
title: "Aspose::Words::Document::get_PackageCustomParts metodo"
linktitle: "get_PackageCustomParts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_PackageCustomParts metodo. Ottiene o imposta la raccolta di parti personalizzate (contenuto arbitrario) che sono collegate al pacchetto OOXML utilizzando \\\"relazioni sconosciute\\\" in C++."
type: docs
weight: 42000
url: /it/cpp/aspose.words/document/get_packagecustomparts/
---
## Document::get_PackageCustomParts method


Ottiene o imposta la raccolta di parti personalizzate (contenuto arbitrario) che sono collegate al pacchetto OOXML usando "relazioni sconosciute".

```cpp
System::SharedPtr<Aspose::Words::Markup::CustomPartCollection> Aspose::Words::Document::get_PackageCustomParts() const
```

## Note


Non confondere queste parti personalizzate con Custom XML Data. Se hai bisogno di accedere a Custom XML parts, usa la proprietà [CustomXmlParts](../get_customxmlparts/).

Questa raccolta contiene parti OOXML il cui genitore è il pacchetto OOXML e i loro obiettivi sono di una \"relazione sconosciuta\". Per ulteriori informazioni, consulta [CustomPart](../../../aspose.words.markup/custompart/).

Aspose.Words carica e salva solo parti personalizzate nei documenti OOXML.

Questa proprietà non può essere **null**.

## Esempi



Mostra come accedere alla raccolta di parti personalizzate arbitrarie di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Custom parts OOXML package.docx");

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

// Clona la seconda parte, quindi aggiungi la copia alla raccolta.
System::SharedPtr<Aspose::Words::Markup::CustomPart> clonedPart = doc->get_PackageCustomParts()->idx_get(1)->Clone();
doc->get_PackageCustomParts()->Add(clonedPart);

ASSERT_EQ(3, doc->get_PackageCustomParts()->get_Count());

// Enumera la raccolta e stampa ogni parte.
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

// Possiamo rimuovere gli elementi da questa raccolta individualmente o tutti insieme.
doc->get_PackageCustomParts()->RemoveAt(2);

ASSERT_EQ(2, doc->get_PackageCustomParts()->get_Count());

doc->get_PackageCustomParts()->Clear();

ASSERT_EQ(0, doc->get_PackageCustomParts()->get_Count());
```

## Vedi anche

* Class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
