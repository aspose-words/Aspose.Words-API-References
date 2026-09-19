---
title: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel metodo"
linktitle: "get_CaptionlessTableOfFiguresLabel"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel metodo. Ottiene o imposta il nome dell'identificatore di sequenza usato quando si crea una tabella delle figure che non include l'etichetta e il numero della didascalia in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/fieldtoc/get_captionlesstableoffigureslabel/
---
## FieldToc::get_CaptionlessTableOfFiguresLabel method


Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella delle figure che non include l'etichetta e il numero della didascalia.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel()
```


## Esempi



Mostra come impostare il nome dell'identificatore di sequenza.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));
fieldToc->set_CaptionlessTableOfFiguresLabel(u"Test");

ASSERT_EQ(u" TOC  \\a Test", fieldToc->GetFieldCode());
```

## Vedi anche

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
