---
title: "Aspose::Words::TextColumnCollection klass"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TextColumnCollection klass. En samling av TextColumn-objekt som representerar alla textkolumner i ett avsnitt av ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 71000
url: /sv/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


En samling av [TextColumn](../textcolumn/) objekt som representerar alla textkolumner i ett avsnitt av ett dokument. För att lära dig mer, besök dokumentationsartikeln [Arbeta med avsnitt](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Count](./get_count/)() | Hämtar antalet kolumner i avsnittet i ett dokument. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Sant om textkolumnerna har lika bredd och är jämnt fördelade. |
| [get_LineBetween](./get_linebetween/)() | När **true**, läggs en vertikal linje till mellan kolumnerna. |
| [get_Spacing](./get_spacing/)() | När kolumnerna är jämnt fördelade, hämtas eller sätts mängden utrymme mellan varje kolumn i punkter. |
| [get_Width](./get_width/)() | När kolumnerna är jämnt fördelade, hämtas bredden på kolumnerna. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returnerar en textkolumn på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Sättare för [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Sättare för [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Sättare för [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Arrangerar text i det angivna antalet textkolumner. |
| static [Type](./type/)() |  |
## Anmärkningar


Använd [SetCount()](./setcount/) för att ange antalet textkolumner.

För att göra alla kolumner lika breda och jämnt fördelade, sätt [EvenlySpaced](./get_evenlyspaced/) till **true** och ange mängden utrymme mellan kolumnerna i [Spacing](./get_spacing/). MS Word kommer automatiskt att beräkna kolumnbredder.

Om du har [EvenlySpaced](./get_evenlyspaced/) satt till **false**, måste du ange bredd och avstånd för varje kolumn individuellt. Använd indexeraren för att komma åt enskilda [TextColumn](../textcolumn/)‑objekt.

När du använder anpassade kolumnbredder, se till att summan av alla kolumnbredder och avstånden mellan dem är lika med sidbredden minus vänstra och högra sidmarginaler.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
