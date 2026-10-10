---
title: "Metodo Aspose::Words::ImportFormatOptions::get_MergePastedLists"
linktitle: "get_MergePastedLists"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ImportFormatOptions::get_MergePastedLists. Ottiene o imposta un valore booleano che specifica se le liste incollate saranno unite alle liste circostanti. Il valore predefinito è false in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/importformatoptions/get_mergepastedlists/
---
## ImportFormatOptions::get_MergePastedLists method


Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti agli elenchi circostanti. Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_MergePastedLists() const
```


## Esempi



Mostra come unire le liste da un documento.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_MergePastedLists(true);

// Imposta la proprietà "MergePastedLists" su "true"; le liste incollate saranno unite alle liste circostanti.
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

dstDoc->Save(get_ArtifactsDir() + u"Document.MergePastedLists.docx");
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
