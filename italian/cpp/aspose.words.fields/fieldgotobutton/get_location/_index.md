---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location metodo"
linktitle: "get_Location"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location metodo. Ottiene o imposta il nome di un segnalibro, di un numero di pagina o di qualche altro elemento a cui saltare in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


Ottiene o imposta il nome di un segnalibro, di un numero di pagina o di qualche altro elemento a cui saltare.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## Esempi



Mostra come inserire un campo GOTOBUTTON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi un campo GOTOBUTTON. Quando facciamo doppio clic su questo campo in Microsoft Word,
// porterà il cursore del testo al segnalibro il cui nome è riferito dalla proprietà Location.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Inserisci un segnalibro valido a cui il campo fare riferimento.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Vedi anche

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
