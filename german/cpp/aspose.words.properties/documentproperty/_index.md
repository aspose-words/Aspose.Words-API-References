---
title: "Aspose::Words::Properties::DocumentProperty Klasse"
linktitle: "DocumentProperty"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Properties::DocumentProperty Klasse. Stellt eine benutzerdefinierte oder integrierte Dokumenteigenschaft dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.properties/documentproperty/
---
## DocumentProperty class


Stellt eine benutzerdefinierte oder integrierte Dokumenteigenschaft dar. Weitere Informationen finden Sie im Dokumentationsartikel [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentProperty : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_IsLinkToContent](./get_islinktocontent/)() | Zeigt, ob diese Eigenschaft mit Inhalt verknüpft ist oder nicht. |
| [get_LinkSource](./get_linksource/)() const | Ermittelt die Quelle einer verknüpften benutzerdefinierten Dokumenteigenschaft. |
| [get_Name](./get_name/)() const | Gibt den Namen der Eigenschaft zurück. |
| [get_Type](./get_type/)() const | Ermittelt den Datentyp der Eigenschaft. |
| [get_Value](./get_value/)() | Liest oder setzt den Wert der Eigenschaft. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Value](./set_value/)(const System::SharedPtr\<System::Object\>\&) | Setter für [Aspose::Words::Properties::DocumentProperty::get_Value](./get_value/). |
| [ToBool](./tobool/)() | Gibt den Eigenschaftswert als bool zurück. |
| [ToByteArray](./tobytearray/)() | Gibt den Eigenschaftswert als Byte‑Array zurück. |
| [ToDateTime](./todatetime/)() | Gibt den Eigenschaftswert als **DateTime** in UTC zurück. |
| [ToDouble](./todouble/)() | Gibt den Eigenschaftswert als double zurück. |
| [ToInt](./toint/)() | Gibt den Eigenschaftswert als integer zurück. |
| [ToString](./tostring/)() const override | Gibt den Eigenschaftswert als Zeichenkette zurück, die gemäß dem aktuellen Gebietsschema formatiert ist. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
