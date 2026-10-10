---
title: "Aspose::Words::TextColumnCollection::SetCount Methode"
linktitle: "SetCount"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::TextColumnCollection::SetCount Methode. Ordnet den Text in die angegebene Anzahl von Textspalten in C++ ein."
type: docs
weight: 13000
url: /de/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Ordnet den Text in die angegebene Anzahl von Textspalten ein.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| newCount | int32_t | Die Anzahl der Spalten, in die der Text angeordnet werden soll. |
## Hinweise


Wenn [EvenlySpaced](../get_evenlyspaced/) **false** ist und Sie die Anzahl der Spalten erhöhen, werden neue [TextColumn](../../textcolumn/) Objekte mit null Breite und Abstand erstellt. Sie müssen Breite und Abstand für die neuen Spalten festlegen.

## Beispiele



Zeigt, wie man mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt.
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

## Siehe auch

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
