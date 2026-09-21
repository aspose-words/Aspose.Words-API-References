---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph‑metod"
linktitle: "MoveToParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph‑metod. Flyttar markören till ett stycke i den aktuella sektionen i C++."
type: docs
weight: 59000
url: /sv/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Flyttar markören till ett stycke i den aktuella sektionen.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| paragraphIndex | int32_t | Indexet för stycket att flytta till. |
| characterIndex | int32_t | Indexet för tecknet i stycket. Ett negativt värde låter dig ange en position från slutet av stycket. Använd -1 för att flytta till slutet av stycket. |
## Anmärkningar


Navigeringen utförs inom den aktuella berättelsen i den aktuella sektionen. Det vill säga, om du flyttade markören till den primära rubriken i den första sektionen, så specificerade *paragraphIndex* indexet för stycket i den rubriken i den sektionen.

När *paragraphIndex* är större än eller lika med 0 anger det ett index från början av sektionen där 0 är det första stycket. När *paragraphIndex* är mindre än 0 anger det ett index från slutet av sektionen där -1 är det sista stycket.

## Exempel



Visar hur man flyttar en builders markörposition till ett angivet stycke.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Skapa en dokument‑builder för att redigera dokumentet. Builderns markör,
// vilket är den punkt där den kommer att infoga nya noder när vi anropar dess dokumentkonstruktionsmetoder,
// är för närvarande i början av dokumentet.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Att flytta den markören till ett annat stycke placerar den markören framför det stycket.
builder->MoveToParagraph(2, 0);

// Allt nytt innehåll som vi lägger till kommer att infogas på den punkten.
builder->Writeln(u"This is a new third paragraph. ");
```

## Se även

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
