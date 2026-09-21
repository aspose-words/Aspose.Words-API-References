---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder‑konstruktor"
linktitle: "FieldBuilder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder konstruktor. Initierar en instans av FieldBuilder-klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Initierar en instans av [FieldBuilder](../) klassen.

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Typen av fältet som ska byggas. |

## Exempel



Visar hur man skapar och infogar ett fält med en fältbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ett bekvämt sätt att lägga till textinnehåll i ett dokument är med en dokumentbyggare.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Fält har sin byggare, som vi kan använda för att konstruera en fältkod bit för bit.
// I det här fallet kommer vi att konstruera ett BARCODE-fält som representerar en amerikansk postkod,
// och sedan infoga det framför ett Run.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Se även

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
