---
title: "Aspose::Words::Markup::CustomXmlPartCollection classe"
linktitle: "CustomXmlPartCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlPartCollection classe. Rappresenta una collezione di Parti XML Personalizzate. Gli elementi sono oggetti CustomXmlPart. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class


Rappresenta una collezione di Parti XML Personalizzate. Gli elementi sono oggetti [CustomXmlPart](../customxmlpart/). Per saperne di più, visita l'articolo della documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Aggiunge un elemento alla raccolta. |
| [Add](./add/)(const System::String\&, const System::String\&) | Crea una nuova parte XML con l'XML specificato e la aggiunge alla collezione. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Clone](./clone/)() | Crea una copia profonda di questa collezione e dei suoi elementi. |
| [CustomXmlPartCollection](./customxmlpartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetById](./getbyid/)(const System::String\&) | Trova e restituisce una parte XML personalizzata in base al suo identificatore. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta un elemento all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Ottiene o imposta un elemento all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un elemento all'indice specificato. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Note


Normalmente non è necessario creare istanze di questa classe. È possibile accedere ai dati XML personalizzati memorizzati in un documento tramite la proprietà [CustomXmlParts](../../aspose.words/document/get_customxmlparts/).

## Esempi



Mostra come creare un tag di documento strutturato con dati XML personalizzati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Costruisci una parte XML che contiene dati e aggiungila alla collezione del documento.
// Se abiliti la scheda "Developer" in Microsoft Word,
// possiamo trovare gli elementi di questa collezione nel "Pannello di mappatura XML", insieme a pochi elementi predefiniti.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Di seguito sono due modi per fare riferimento alle parti XML.
// 1 -  Per indice nella collezione delle parti XML personalizzate:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Per GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Aggiungi un'associazione di schema XML.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Clona una parte, quindi inseriscila nella collezione.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Itera attraverso la collezione e stampa il contenuto di ogni parte.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Usa il metodo "RemoveAt" per rimuovere la parte clonata per indice.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Clona la collezione delle parti XML, quindi usa il metodo "Clear" per rimuovere tutti i suoi elementi in una volta.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Crea un tag di documento strutturato che visualizzi il contenuto della nostra parte e inseriscilo nel corpo del documento.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
