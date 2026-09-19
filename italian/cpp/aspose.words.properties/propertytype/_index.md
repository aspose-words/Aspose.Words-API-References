---
title: "Aspose::Words::Properties::PropertyType enum"
linktitle: "PropertyType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Properties::PropertyType enum. Specifica il tipo di dato di una proprietà del documento in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.properties/propertytype/
---
## PropertyType enum


Specifica il tipo di dati di una proprietà del documento.

```cpp
enum class PropertyType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Boolean | 0 | La proprietà è un valore booleano. |
| DateTime | 1 | La proprietà è un valore di data e ora. |
| Doppia | 2 | La proprietà è un numero a virgola mobile. |
| Number | 3 | La proprietà è un numero intero. |
| String | 4 | La proprietà è un valore stringa. |
| StringArray | 5 | La proprietà è un array di stringhe. |
| ObjectArray | 6 | La proprietà è un array di oggetti. |
| ByteArray | 7 | La proprietà è un array di byte. |
| Altro | 8 | La proprietà è di qualche altro tipo. |


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
