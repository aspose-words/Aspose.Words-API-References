---
title: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter metodo"
linktitle: "get_SeparatorCharacter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter method. Ottiene o imposta il carattere separatore da utilizzare in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldautonum/get_separatorcharacter/
---
## FieldAutoNum::get_SeparatorCharacter method


Ottiene o imposta il carattere separatore da utilizzare.

```cpp
System::String Aspose::Words::Fields::FieldAutoNum::get_SeparatorCharacter()
```


## Esempi



Mostra come numerare i paragrafi usando campi autonum.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ogni campo AUTONUM visualizza il valore corrente di un conteggio progressivo di campi AUTONUM,
// consentendoci di numerare automaticamente gli elementi come in un elenco numerato.
// Questo campo visualizzerà il numero "1.".
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 1.");

ASSERT_EQ(u" AUTONUM ", field->GetFieldCode());

field = System::ExplicitCast<Aspose::Words::Fields::FieldAutoNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNum, true));
builder->Writeln(u"\tParagraph 2.");

// Il carattere separatore, che appare nel risultato del campo immediatamente dopo il numero, è un punto per impostazione predefinita.
// Se lasciamo questa proprietà null, il nostro secondo campo AUTONUM visualizzerà "2." nel documento.
ASSERT_TRUE(System::TestTools::IsNull(field->get_SeparatorCharacter()));

// Possiamo impostare questa proprietà per utilizzare il primo carattere della sua stringa come nuovo carattere separatore.
// In questo caso, il nostro campo AUTONUM visualizzerà ora "2:".
field->set_SeparatorCharacter(u":");

ASSERT_EQ(u" AUTONUM  \\s :", field->GetFieldCode());

doc->Save(get_ArtifactsDir() + u"Field.AUTONUM.docx");
```

## Vedi anche

* Class [FieldAutoNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
