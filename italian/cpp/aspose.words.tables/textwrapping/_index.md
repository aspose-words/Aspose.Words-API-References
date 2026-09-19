---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::TextWrapping enum. Specifica come il testo viene avvolto attorno alla tabella in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Specifica come il testo viene avvolto attorno alla tabella.

```cpp
enum class TextWrapping
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Il testo e la tabella vengono visualizzati nell'ordine della loro comparsa nel documento. |
| Intorno | 1 | Il testo è avvolto attorno alla tabella occupando lo spazio laterale disponibile. |
| Default | n/a | Valore predefinito. |


## Esempi



Mostra come lavorare con l'avvolgimento del testo nella tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Imposta la proprietà "TextWrapping" su "TextWrapping.Around" per far avvolgere il testo attorno alla tabella,
// e spostala verso il basso nel paragrafo sottostante impostando la posizione.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
