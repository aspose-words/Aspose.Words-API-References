---
title: "Aspose::Words::Markup::CustomPart class"
linktitle: "CustomPart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomPart class. Stellt einen benutzerdefinierten (beliebigen Inhalt) Teil dar, der nicht durch den ISO/IEC 29500-Standard definiert ist. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Stellt einen benutzerdefinierten (beliebigen Inhalt) Teil dar, der nicht durch den ISO/IEC‑29500‑Standard definiert ist. Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Erstellt eine „deep enough“-Kopie des Objekts. Dupliziert nicht die Bytes des [Data](./get_data/)-Werts. |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Gibt den Inhaltstyp dieses benutzerdefinierten Teils an. |
| [get_Data](./get_data/)() const | Enthält die Daten dieses benutzerdefinierten Teils. |
| [get_IsExternal](./get_isexternal/)() const | Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. Wahr, wenn dieser benutzerdefinierte Teil ein externes Ziel ist. |
| [get_Name](./get_name/)() const | Liest oder setzt den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder die Ziel-URL. |
| [get_RelationshipType](./get_relationshiptype/)() const | Liest oder setzt den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Setter für [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Setter für [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Setter für [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Setter für [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Hinweise


Diese Klasse stellt einen OOXML-Teil dar, der Ziel einer "unbekannten Beziehung" ist. Alle Beziehungen, die nicht im ISO/IEC 29500 definiert sind, gelten als "unbekannte Beziehungen". Unbekannte Beziehungen sind in einem Office Open XML-Dokument zulässig, sofern sie den Richtlinien für Beziehungs-Markup entsprechen.

Microsoft Word bewahrt benutzerdefinierte Teile während Öffnen-/Speichern-Zyklen. Weitere Informationen finden Sie hier [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words führt benutzerdefinierte Teile ebenfalls unverändert durch (Round‑Trip) und ermöglicht zusätzlich den programmgesteuerten Zugriff auf solche Teile über die Objekte [CustomPart](./) und [CustomPartCollection](../custompartcollection/).

Verwechseln Sie benutzerdefinierte Teile nicht mit benutzerdefinierten XML-Daten. Verwenden Sie [CustomXmlPart](../customxmlpart/), wenn Sie auf benutzerdefinierte XML-Daten zugreifen müssen.

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
