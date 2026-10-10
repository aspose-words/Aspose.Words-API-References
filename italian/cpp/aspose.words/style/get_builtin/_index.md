---
title: "Metodo Aspose::Words::Style::get_BuiltIn"
linktitle: "get_BuiltIn"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_BuiltIn. True se questo stile è uno degli stili predefiniti in MS Word in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/style/get_builtin/
---
## Style::get_BuiltIn method


Vero se questo stile è uno degli stili integrati in MS Word.

```cpp
bool Aspose::Words::Style::get_BuiltIn()
```


## Esempi



Mostra come differenziare gli stili personalizzati dagli stili predefiniti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Quando creiamo un documento usando Microsoft Word, o programmaticamente usando Aspose.Words,
// il documento includerà una raccolta di stili da applicare al suo testo per modificarne l'aspetto.
// Possiamo accedere a questi stili predefiniti tramite la raccolta "Styles" del documento.
// Tutti questi stili avranno il flag "BuiltIn" impostato su "true".
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"Emphasis");

ASSERT_TRUE(style->get_BuiltIn());

// Crea uno stile personalizzato e aggiungilo alla raccolta.
// Gli stili personalizzati come questo avranno il flag "BuiltIn" impostato su "false".
style = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"MyStyle");
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
style->get_Font()->set_Name(u"Courier New");

ASSERT_FALSE(style->get_BuiltIn());
```

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
