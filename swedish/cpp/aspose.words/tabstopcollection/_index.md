---
title: "Aspose::Words::TabStopCollection klass"
linktitle: "TabStopCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::TabStopCollection klass. En samling av TabStop-objekt som representerar anpassade tabbar för ett stycke eller en stil. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 69000
url: /sv/cpp/aspose.words/tabstopcollection/
---
## TabStopCollection class


En samling av [TabStop](../tabstop/) objekt som representerar anpassade tabbar för ett stycke eller en stil. För att lära dig mer, besök [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) dokumentationsartikel.

```cpp
class TabStopCollection : public Aspose::Words::InternableComplexAttr,
                          public Aspose::Words::IExpandableAttr
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::TabStop\>\&) | Lägger till eller ersätter ett tabbstopp i samlingen. |
| [Add](./add/)(double, Aspose::Words::TabAlignment, Aspose::Words::TabLeader) | Lägger till eller ersätter ett tabbstopp i samlingen. |
| [After](./after/)(double) | Hämtar det första tabbstoppet till höger om den angivna positionen. |
| [Before](./before/)(double) | Hämtar det första tabbstoppet till vänster om den angivna positionen. |
| [Clear](./clear/)() | Raderar alla tabbstopppositioner. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::TabStopCollection\>\&) | Avgör om den angivna [TabStopCollection](./) är lika i värde med den aktuella [TabStopCollection](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_Count](./get_count/)() | Hämtar antalet tabbstopp i samlingen. |
| [GetHashCode](./gethashcode/)() const override | Fungerar som en hash-funktion för denna typ. |
| [GetIndexByPosition](./getindexbyposition/)(double) | Hämtar indexet för ett tabbstopp med den angivna positionen i punkter. |
| [GetPositionByIndex](./getpositionbyindex/)(int32_t) | Hämtar positionen (i punkter) för tabbstoppet på det angivna indexet. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar ett tabbstopp på det angivna indexet. |
| [idx_get](./idx_get/)(double) | Hämtar ett tabbstopp på den angivna positionen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveByIndex](./removebyindex/)(int32_t) | Tar bort ett tabbstopp på det angivna indexet från samlingen. |
| [RemoveByPosition](./removebyposition/)(double) | Tar bort ett tabbstopp på den angivna positionen från samlingen. |
| static [Type](./type/)() |  |
## Anmärkningar


I Microsoft Word-dokument kan ett tabbstopp definieras i egenskaperna för ett styckeformat eller direkt i egenskaperna för ett stycke. Ett format kan baseras på ett annat format. Därför är den kompletta uppsättningen av tabbstopp för ett givet objekt en kombination av tabbstopp som definierats direkt på detta objekt och tabbstopp som ärvts från föräldraformaten.

I Aspose.Words, när du hämtar en [TabStopCollection](./) för ett stycke eller ett format, innehåller den endast de anpassade tabbstoppen som definierats direkt för detta stycke eller format. Samlingen inkluderar inte tabbstopp som definierats i föräldraformaten eller standardtabbstopp.

## Exempel



Visar hur man arbetar med ett dokuments samling av tabbstopp.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = builder->get_ParagraphFormat()->get_TabStops();

// 72 punkter är en "tum" på Microsoft Word:s tabbstopp-linjal.
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(72.0));
tabStops->Add(System::MakeObject<Aspose::Words::TabStop>(432.0, Aspose::Words::TabAlignment::Right, Aspose::Words::TabLeader::Dashes));

ASSERT_EQ(2, tabStops->get_Count());
ASSERT_FALSE(tabStops->idx_get(0)->get_IsClear());
ASSERT_FALSE(System::ObjectExt::Equals(tabStops->idx_get(0), tabStops->idx_get(1)));

// Varje "tab"-tecken flyttar byggarens markör till platsen för nästa tabbstopp.
builder->Writeln(u"Start\tTab 1\tTab 2");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(2, paragraphs->get_Count());

// Varje stycke får sin tabbstopp-samling, som klonar sina värden från dokumentbyggarens tabbstopp-samling.
ASPOSE_ASSERT_EQ(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());
ASPOSE_ASSERT_NS(paragraphs->idx_get(0)->get_ParagraphFormat()->get_TabStops(), paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops());

// En samling tabbstopp kan peka oss till TabStops före och efter vissa positioner.
ASPOSE_ASSERT_EQ(72.0, tabStops->Before(100.0)->get_Position());
ASPOSE_ASSERT_EQ(432.0, tabStops->After(100.0)->get_Position());

// Vi kan rensa ett styckes tabbstoppsamling för att återgå till standardtabb‑beteendet.
paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->Clear();

ASSERT_EQ(0, paragraphs->idx_get(1)->get_ParagraphFormat()->get_TabStops()->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.TabStopCollection.docx");
```

## Se även

* Class [InternableComplexAttr](../internablecomplexattr/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
