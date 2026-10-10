---
title: "Metodo Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks"
linktitle: "get_ShowParagraphMarks"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks. Ottiene o imposta l'indicazione se i segni di paragrafo sono visualizzati. Il valore predefinito è false in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.layout/layoutoptions/get_showparagraphmarks/
---
## LayoutOptions::get_ShowParagraphMarks method


Ottiene o imposta l'indicazione se i segni di paragrafo vengono visualizzati. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks() const
```


## Esempi



Mostra come visualizzare i segni di paragrafo in un documento di output renderizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi alcuni paragrafi, quindi abilita i segni di paragrafo per mostrare le fine dei paragrafi
// con il simbolo pilcrow (¶) quando renderizziamo il documento.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```

## Vedi anche

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
