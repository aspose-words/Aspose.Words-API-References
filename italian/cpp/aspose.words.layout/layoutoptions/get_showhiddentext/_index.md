---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText"
linktitle: "get_ShowHiddenText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText. Ottiene o imposta l'indicazione se il testo nascosto nel documento è visualizzato. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.layout/layoutoptions/get_showhiddentext/
---
## LayoutOptions::get_ShowHiddenText method


Ottiene o imposta l'indicazione se il testo nascosto nel documento viene visualizzato. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText() const
```


## Esempi



Mostra come nascondere il testo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci testo nascosto, quindi specifica se desideriamo ometterlo da un documento renderizzato.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```

## Vedi anche

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
