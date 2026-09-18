---
title: "Aspose::Words::Document::get_BuiltInDocumentProperties method"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Document::get_BuiltInDocumentProperties-Methode. Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments in C++ darstellt."
type: docs
weight: 15000
url: /de/cpp/aspose.words/document/get_builtindocumentproperties/
---
## Document::get_BuiltInDocumentProperties method


Gibt eine Sammlung zurück, die alle integrierten Dokumenteigenschaften des Dokuments repräsentiert.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::Document::get_BuiltInDocumentProperties() const
```


## Beispiele



Zeigt, wie man mit integrierten Dokumenteigenschaften arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Properties.docx");

// Das "Document"-Objekt enthält einige seiner Metadaten in seinen Mitgliedern.
std::cout << System::String::Format(u"Document filename:\n\t \"{0}\"", doc->get_OriginalFileName()) << std::endl;

// Das Dokument speichert Metadaten auch in seinen integrierten Eigenschaften.
// Jede integrierte Eigenschaft ist ein Mitglied des "BuiltInDocumentProperties"-Objekts des Dokuments.
std::cout << "Built-in Properties:" << std::endl;
for (auto&& docProperty : System::IterateOver(doc->get_BuiltInDocumentProperties()))
{
    std::cout << docProperty->get_Name() << std::endl;
    std::cout << System::String::Format(u"\tType:\t{0}", docProperty->get_Type()) << std::endl;

    // Einige Eigenschaften können mehrere Werte speichern.
    if (System::ObjectExt::Is<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value()))
    {
        for (auto&& value : System::IterateOver(System::AsCast<System::Collections::Generic::ICollection<System::SharedPtr<System::Object>>>(docProperty->get_Value())))
        {
            std::cout << System::String::Format(u"\tValue:\t\"{0}\"", value) << std::endl;
        }
    }
    else
    {
        std::cout << System::String::Format(u"\tValue:\t\"{0}\"", docProperty->get_Value()) << std::endl;
    }
}
```

## Siehe auch

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
