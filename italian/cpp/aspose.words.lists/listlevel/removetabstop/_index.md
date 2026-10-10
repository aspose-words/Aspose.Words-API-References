---
title: "Aspose::Words::Lists::ListLevel::RemoveTabStop metodo"
linktitle: "RemoveTabStop"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Lists::ListLevel::RemoveTabStop metodo. Rimuove la tabulazione dal livello dell'elenco in C++."
type: docs
weight: 22500
url: /it/cpp/aspose.words.lists/listlevel/removetabstop/
---
## ListLevel::RemoveTabStop method


Rimuove la tabulazione dal livello di elenco.

```cpp
void Aspose::Words::Lists::ListLevel::RemoveTabStop()
```


## Esempi



Mostra come cancellare la tabulazione del livello dell'elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un elenco con formattazione predefinita
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");

// Ottieni il livello dell'elenco e rimuovi la sua tabulazione
System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = builder->get_ListFormat()->get_ListLevel();
listLevel->RemoveTabStop();

doc->Save(get_ArtifactsDir() + u"Paragraph.RemoveTabStopFromListLevel.docx");
```

## Vedi anche

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
