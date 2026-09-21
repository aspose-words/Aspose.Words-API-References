---
title: "Aspose::Words::DocumentBuilder::MoveToSection‑metod"
linktitle: "MoveToSection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToSection‑metod. Flyttar markören till början av kroppen i en angiven sektion i C++."
type: docs
weight: 60000
url: /sv/cpp/aspose.words/documentbuilder/movetosection/
---
## DocumentBuilder::MoveToSection method


Flyttar markören till början av kroppen i en angiven sektion.

```cpp
void Aspose::Words::DocumentBuilder::MoveToSection(int32_t sectionIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sectionIndex | int32_t | Indexet för sektionen att flytta till. |
## Anmärkningar


När *sectionIndex* är större än eller lika med 0 specificerar den ett index från början av dokumentet där 0 är den första sektionen. När *sectionIndex* är mindre än 0 specificerar den ett index från slutet av dokumentet där -1 är den sista sektionen.

Markören flyttas till det första stycket i [Body](../../body/) för den angivna sektionen.

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
