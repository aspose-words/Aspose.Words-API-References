---
title: "Aspose::Words::Properties::DocumentPropertyCollection‑klass"
linktitle: "DocumentPropertyCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Properties::DocumentPropertyCollection‑klass. Basisklass för samlingarna BuiltInDocumentProperties och CustomDocumentProperties. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class


Basisklass för samlingarna [BuiltInDocumentProperties](../builtindocumentproperties/) och [CustomDocumentProperties](../customdocumentproperties/). För att lära dig mer, besök dokumentationsartikeln [Work with Document Properties](https://docs.aspose.com/words/cpp/work-with-document-properties/).

```cpp
class DocumentPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clear](./clear/)() | Tar bort alla egenskaper från samlingen. |
| [Contains](./contains/)(const System::String\&) | Returnerar **true** om en egenskap med det angivna namnet finns i samlingen. |
| [get_Count](./get_count/)() | Hämtar antalet objekt i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| virtual [idx_get](./idx_get/)(System::String) | Returnerar ett [DocumentProperty](../documentproperty/)-objekt med egenskapens namn. |
| [idx_get](./idx_get/)(int32_t) | Returnerar ett [DocumentProperty](../documentproperty/)-objekt efter index. |
| [IndexOf](./indexof/)(const System::String\&) | Hämtar indexet för en egenskap efter namn. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort en egenskap på det angivna indexet. |
| static [Type](./type/)() |  |
## Anmärkningar


Namnen på egenskaperna är skiftlägesokänsliga.

Egenskaperna i samlingen sorteras alfabetiskt efter namn.

## Exempel



Visar hur man arbetar med ett dokuments anpassade egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> properties = doc->get_CustomDocumentProperties();

ASSERT_EQ(0, properties->get_Count());

// Anpassade dokumentegenskaper är nyckel‑värde‑par som vi kan lägga till i dokumentet.
properties->Add(u"Authorized", true);
properties->Add(u"Authorized By", System::String(u"John Doe"));
properties->Add(u"Authorized Date", System::DateTime::get_Today());
properties->Add(u"Authorized Revision", doc->get_BuiltInDocumentProperties()->get_RevisionNumber());
properties->Add(u"Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
ASSERT_EQ(1, properties->IndexOf(u"Authorized Amount"));
ASSERT_EQ(5, properties->get_Count());

// Skriv ut varje anpassad egenskap i dokumentet.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Properties::DocumentProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Name: \"{0}\"\n\tType: \"{1}\"\n\tValue: \"{2}\"", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Type(), enumerator->get_Current()->get_Value()) << std::endl;
    }
}

// Visa värdet av en anpassad egenskap med ett DOCPROPERTY-fält.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY \"Authorized By\""));
field->Update();

ASSERT_EQ(u"John Doe", field->get_Result());

// Vi kan hitta dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassade".
doc->Save(get_ArtifactsDir() + u"DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 -  Ta bort efter index:
properties->RemoveAt(1);

ASSERT_FALSE(properties->Contains(u"Authorized Amount"));
ASSERT_EQ(4, properties->get_Count());

// 2 -  Ta bort efter namn:
properties->Remove(u"Authorized Revision");

ASSERT_FALSE(properties->Contains(u"Authorized Revision"));
ASSERT_EQ(3, properties->get_Count());

// 3 -  Töm hela samlingen på en gång:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Se även

* Namespace [Aspose::Words::Properties](../)
* Library [Aspose.Words for C++](../../)
