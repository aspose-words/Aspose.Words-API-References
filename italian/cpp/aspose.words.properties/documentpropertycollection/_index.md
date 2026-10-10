---
title: "Classe Aspose::Words::Properties::DocumentPropertyCollection"
linktitle: "DocumentPropertyCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Properties::DocumentPropertyCollection. Classe base per le collezioni BuiltInDocumentProperties e CustomDocumentProperties. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Classe base per le collezioni [BuiltInDocumentProperties](../builtindocumentproperties/) e [CustomDocumentProperties](../customdocumentproperties/). Per saperne di più, visita l'articolo di documentazione [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clear](./clear/)() | Rimuove tutte le proprietà dalla raccolta. |
| [Contains](./contains/)(const System::String\&) | Restituisce **true** se una proprietà con il nome specificato esiste nella raccolta. |
| [get_Count](./get_count/)() | Ottiene il numero di elementi nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Restituisce un oggetto [DocumentProperty](../documentproperty/) per nome della proprietà. |
| [idx_get](./idx_get/)(int32_t) | Restituisce un oggetto [DocumentProperty](../documentproperty/) per indice. |
| [IndexOf](./indexof/)(const System::String\&) | Ottiene l'indice di una proprietà per nome. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove una proprietà all'indice specificato. |
| static [Type](./type/)() |  |
## Note


I nomi delle proprietà non distinguono tra maiuscole e minuscole.

Le proprietà nella raccolta sono ordinate alfabeticamente per nome.

## Esempi



Mostra come lavorare con le proprietà personalizzate di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Le proprietà personalizzate del documento sono coppie chiave-valore che possiamo aggiungere al documento.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// La collezione ordina le proprietà personalizzate in ordine alfabetico.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Stampa ogni proprietà personalizzata nel documento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Visualizza il valore di una proprietà personalizzata usando un campo DOCPROPERTY.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Possiamo trovare queste proprietà personalizzate in Microsoft Word tramite "File" -> "Properties" > "Advanced Properties" > "Custom".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Di seguito sono riportati tre modi per rimuovere le proprietà personalizzate da un documento.
// 1 -  Rimuovi per indice:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Rimuovi per nome:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Svuota l'intera raccolta in una volta:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
