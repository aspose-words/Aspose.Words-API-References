---
title: "Aspose::Words::TextColumnCollection::SetCount metod"
linktitle: "SetCount"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumnCollection::SetCount metod. Arrangerar texten i det angivna antalet textkolumner i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Arrangerar text i det angivna antalet textkolumner.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| newCount | int32_t | Antalet kolumner som texten ska arrangeras i. |
## Anmärkningar


När [EvenlySpaced](../get_evenlyspaced/) är **false** och du ökar antalet kolumner, skapas nya [TextColumn](../../textcolumn/)‑objekt med noll bredd och avstånd. Du måste sätta bredd och avstånd för de nya kolumnerna.

## Exempel



Visar hur man skapar flera jämnt fördelade kolumner i ett avsnitt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Se även

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
