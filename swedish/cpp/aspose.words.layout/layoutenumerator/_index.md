---
title: "Aspose::Words::Layout::LayoutEnumerator klass"
linktitle: "LayoutEnumerator"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Layout::LayoutEnumerator-klass. Enumererar sidlayout‑entiteter i ett dokument. Du kan använda den här klassen för att gå igenom sidlayoutmodellen. Tillgängliga egenskaper är typ, geometri, text och sidindex där entiteten renderas, samt den övergripande strukturen och relationerna. Använd en kombination av GetEntity() och Current för att flytta till den entitet som motsvarar ett dokumentnod. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.layout/layoutenumerator/
---
## LayoutEnumerator class


Enumererar sidlayout‑entiteter i ett dokument. Du kan använda den här klassen för att gå igenom sidlayoutmodellen. Tillgängliga egenskaper är typ, geometri, text och sidindex där entiteten renderas, samt den övergripande strukturen och relationerna. Använd en kombination av [GetEntity()](../) och [Current](./get_current/) för att flytta till den entitet som motsvarar ett dokumentnod. För att lära dig mer, besök dokumentationsartikeln [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutEnumerator : public System::Object,
                         public System::Details::EnumeratorBasedIterator<System::SharedPtr<System::Object>>,
                         private System::Details::IteratorPointerUpdater<System::SharedPtr<System::Object>, false>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CloneIterator](./cloneiterator/)() const override |  |
| [get_Current](./get_current/)() const | Hämtar eller anger aktuell position i sidlayoutmodellen. Denna egenskap returnerar ett opakt objekt som motsvarar den aktuella layout‑entiteten. |
| [get_Document](./get_document/)() const | Hämtar dokumentet som detta objekt enumererar. |
| [get_Kind](./get_kind/)() | Hämtar typen av den aktuella entiteten. Detta kan vara en tom sträng men aldrig **null**. |
| [get_PageIndex](./get_pageindex/)() | Hämtar det 1‑baserade indexet för en sida som innehåller den aktuella entiteten. |
| [get_Rectangle](./get_rectangle/)() | Returnerar den omgivande rektangeln för den aktuella entiteten relativt sidans övre vänstra hörn (i punkter). |
| [get_Text](./get_text/)() | Hämtar texten för den aktuella span‑entiteten. Kastar undantag för andra entitetstyper. |
| [get_Type](./get_type/)() | Hämtar typen av den aktuella entiteten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar en namngiven egenskap för entiteten. |
| [IncrementIterator](./incrementiterator/)() override |  |
| [InitializeIterator](./initializeiterator/)() override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutEnumerator](./layoutenumerator/)(const System::SharedPtr\<Aspose::Words::Document\>\&) | Initierar en ny instans av denna klass. |
| [MoveFirstChild](./movefirstchild/)() | Flyttar till den första underordnade entiteten. |
| [MoveLastChild](./movelastchild/)() | Flyttar till den sista underordnade entiteten. |
| [MoveNext](./movenext/)() | Flyttar till nästa syskonentitet i visuell ordning. När man itererar rader i ett stycke som bryts över sidor kommer denna metod inte att gå till nästa sida utan istället gå till nästa entitet på samma sida. |
| [MoveNextLogical](./movenextlogical/)() | Flyttar till nästa syskonentitet i logisk ordning. När man itererar rader i ett stycke som bryts över sidor kommer denna metod att gå till nästa rad även om den finns på en annan sida. |
| [MoveParent](./moveparent/)() | Flyttar till föräldraentiteten. |
| [MoveParent](./moveparent/)(Aspose::Words::Layout::LayoutEntityType) | Flyttar till föräldraentiteten av den angivna typen. |
| [MovePrevious](./moveprevious/)() | Flyttar till föregående syskonentitet. |
| [MovePreviousLogical](./movepreviouslogical/)() | Flyttar till föregående syskonentitet i logisk ordning. När man itererar rader i ett stycke som bryts över sidor kommer denna metod att gå till föregående rad även om den finns på en annan sida. |
| [Reset](./reset/)() | Flyttar enumeratorn till den första sidan i dokumentet. |
| [set_Current](./set_current/)(const System::SharedPtr\<System::Object\>\&) | Sättare för [Aspose::Words::Layout::LayoutEnumerator::get_Current](./get_current/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
