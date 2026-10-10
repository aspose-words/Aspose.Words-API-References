---
title: "Aspose::Words::DocumentBuilder::MoveToCell metod"
linktitle: "MoveToCell"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToCell metod. Flyttar markören till en tabellcell i den aktuella sektionen i C++."
type: docs
weight: 53000
url: /sv/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Flyttar markören till en tabellcell i den aktuella sektionen.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableIndex | int32_t | Index för tabellen att flytta till. |
| rowIndex | int32_t | Index för raden i tabellen. |
| columnIndex | int32_t | Index för kolumnen i tabellen. |
| characterIndex | int32_t | Index för tecknet i cellen. Ett negativt värde låter dig ange en position från slutet av cellen. Använd -1 för att flytta till slutet av cellen. |
## Anmärkningar


Navigeringen utförs inom den aktuella berättelsen i den aktuella sektionen.

För indexparametrarna, när index är större än eller lika med 0, anger det ett index från början där 0 är det första elementet. När index är mindre än 0, anger det ett index från slutet där -1 är det sista elementet.

## Exempel



Visar hur man flyttar en document builder's markör till en cell i en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en tom 2x2-tabell.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Eftersom vi har avslutat tabellen med EndTable-metoden,
// är document builder's markör för närvarande utanför tabellen.
// Den här markören har samma funktion som Microsoft Words blinkande textmarkör.
// Den kan också flyttas till en annan plats i dokumentet med hjälp av builderns MoveTo‑metoder.
// Vi kan flytta markören tillbaka in i tabellen till en specifik cell.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
