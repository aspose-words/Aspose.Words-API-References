---
title: "Aspose::Words::TabStopCollection::RemoveByIndex metodo"
linktitle: "RemoveByIndex"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TabStopCollection::RemoveByIndex metodo. Rimuove una tabulazione all'indice specificato dalla collezione in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


Rimuove una tabulazione all'indice specificato dalla raccolta.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella raccolta di tabulazioni. |

## Esempi



Mostra come selezionare una tabulazione in un documento per indice e rimuoverla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// Rimuovi la prima tabulazione.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## Vedi anche

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
