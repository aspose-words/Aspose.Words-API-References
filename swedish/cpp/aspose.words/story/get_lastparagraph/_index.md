---
title: "Aspose::Words::Story::get_LastParagraph metod"
linktitle: "get_LastParagraph"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Story::get_LastParagraph metod. Hämtar det sista stycket i storyn i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Hämtar det sista stycket i berättelsen.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Exempel



Visar hur man flyttar en [DocumentBuilder](../../documentbuilder/)'s markörposition till en specificerad nod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Dokumentbyggaren har en markör, som fungerar som en del av dokumentet
// där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
// Denna markör fungerar på samma sätt som Microsoft Words blinkande markör,
// och den hamnar också alltid omedelbart efter vilken nod som helst som byggaren just har infogat.
// För att lägga till innehåll i en annan del av dokumentet,
// kan vi flytta markören till en annan nod med metoden "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Markören är nu framför den nod vi flyttade den till.
// Att lägga till en andra körning kommer att infoga den framför den första körningen.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Se även

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
