---
title: "classe Aspose::Words::Markup::CustomPart"
linktitle: "CustomPart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomPart classe. Rappresenta una parte personalizzata (contenuto arbitrario) che non è definita dallo standard ISO/IEC 29500. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.markup/custompart/
---
## CustomPart class


Rappresenta una parte personalizzata (contenuto arbitrario) che non è definita dallo standard ISO/IEC 29500. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomPart : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Crea una copia "deep enough" dell'oggetto. Non duplica i byte del valore [Data](./get_data/). |
| [CustomPart](./custompart/)() |  |
| [get_ContentType](./get_contenttype/)() const | Specifica il tipo di contenuto di questa parte personalizzata. |
| [get_Data](./get_data/)() const | Contiene i dati di questa parte personalizzata. |
| [get_IsExternal](./get_isexternal/)() const | Falso se questa parte personalizzata è memorizzata all'interno del pacchetto OOXML. Vero se questa parte personalizzata è una destinazione esterna. |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome assoluto di questa parte all'interno del pacchetto OOXML o l'URL di destinazione. |
| [get_RelationshipType](./get_relationshiptype/)() const | Ottiene o imposta il tipo di relazione dalla parte padre a questa parte personalizzata. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContentType](./set_contenttype/)(const System::String\&) | Impostatore per [Aspose::Words::Markup::CustomPart::get_ContentType](./get_contenttype/). |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Impostatore per [Aspose::Words::Markup::CustomPart::get_Data](./get_data/). |
| [set_IsExternal](./set_isexternal/)(bool) | Impostatore per [Aspose::Words::Markup::CustomPart::get_IsExternal](./get_isexternal/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Markup::CustomPart::get_Name](./get_name/). |
| [set_RelationshipType](./set_relationshiptype/)(const System::String\&) | Impostatore per [Aspose::Words::Markup::CustomPart::get_RelationshipType](./get_relationshiptype/). |
| static [Type](./type/)() |  |
## Note


Questa classe rappresenta una parte OOXML che è una destinazione di una \"relazione sconosciuta\". Tutte le relazioni non definite nello standard ISO/IEC 29500 sono considerate \"relazioni sconosciute\". Le relazioni sconosciute sono consentite all'interno di un documento Office Open XML a condizione che rispettino le linee guida per il markup delle relazioni.

Microsoft Word conserva le parti personalizzate durante i cicli di apertura/salvataggio. Ulteriori informazioni sono disponibili qui [http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx](http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx)

Aspose.Words effettua anche il round‑trip delle parti personalizzate e, inoltre, consente di accedere programmaticamente a tali parti tramite gli oggetti [CustomPart](./) e [CustomPartCollection](../custompartcollection/).

Non confondere le parti personalizzate con i Dati XML Personalizzati. Usa [CustomXmlPart](../customxmlpart/) se devi accedere ai Dati XML Personalizzati.

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
