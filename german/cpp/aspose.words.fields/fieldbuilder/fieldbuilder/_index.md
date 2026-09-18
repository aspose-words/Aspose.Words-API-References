---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder Konstruktor"
linktitle: "FieldBuilder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder Konstruktor. Initialisiert eine Instanz der FieldBuilder-Klasse in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Initialisiert eine Instanz der [FieldBuilder](../)-Klasse.

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Der Typ des zu erstellenden Feldes. |

## Beispiele



Zeigt, wie man ein Feld mit einem Feld-Builder erstellt und einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine bequeme Möglichkeit, Textinhalt zu einem Dokument hinzuzufügen, ist ein Dokument-Builder.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Felder haben ihren Builder, den wir verwenden können, um einen Feldcode Stück für Stück zu konstruieren.
// In diesem Fall werden wir ein BARCODE-Feld erstellen, das einen US-Postleitzahl darstellt,
// und es dann vor einem Run einfügen.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Siehe auch

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
