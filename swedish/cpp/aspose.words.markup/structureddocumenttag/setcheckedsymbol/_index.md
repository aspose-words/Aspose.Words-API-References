---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol metod"
linktitle: "SetCheckedSymbol"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol metod. Anger symbolen som används för att representera den ikryssade statusen för en kryssruteinnehållskontroll i C++."
type: docs
weight: 58000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag::SetCheckedSymbol method


Anger symbolen som används för att representera det markerade tillståndet för en kryssrutan innehållskontroll.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| characterCode | int32_t | Teckenkoden för den angivna symbolen. |
| fontName | const System::String\& | Namnet på teckensnittet som innehåller symbolen. |
## Anmärkningar


Att anropa denna metod fungerar endast för [Checkbox](../../sdttype/) SDT-typer.

För alla andra SDT-typer kommer ett undantag att uppstå.

## Exempel



Visa hur man skapar en strukturerad dokumenttagg i form av en kryssruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Vi kan ange de symboler som används för att representera kryssad/okryssad status för en kryssruta-innehållskontroll.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
