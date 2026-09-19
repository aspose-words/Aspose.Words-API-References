---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder costruttore"
linktitle: "FieldBuilder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder costruttore. Inizializza un'istanza della classe FieldBuilder in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Inizializza un'istanza della classe [FieldBuilder](../).

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Il tipo del campo da costruire. |

## Esempi



Mostra come creare e inserire un campo utilizzando un field builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un modo comodo per aggiungere contenuto testuale a un documento è con un document builder.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// I campi hanno il loro builder, che possiamo usare per costruire il codice del campo pezzo per pezzo.
// In questo caso, costruiremo un campo BARCODE che rappresenta un codice postale statunitense,
// e poi lo inseriremo davanti a un Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Vedi anche

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
