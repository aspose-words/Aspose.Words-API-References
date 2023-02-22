---
title: StructuredDocumentTag.SetUncheckedSymbol
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTag metod. Ställer in symbolen som används för att representera det omarkerade tillståndet för en innehållskontroll i kryssrutan.
type: docs
weight: 360
url: /sv/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Ställer in symbolen som används för att representera det omarkerade tillståndet för en innehållskontroll i kryssrutan.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| characterCode | Int32 | Teckenkoden för den angivna symbolen. |
| fontName | String | Namnet på teckensnittet som innehåller symbolen. |

### Anmärkningar

Att komma åt den här metoden fungerar bara förCheckbox SDT-typer.

För alla andra SDT-typer kommer undantag att förekomma.

### Exempel

Visa hur man skapar en strukturerad dokumenttagg i form av en kryssruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Vi kan ställa in de symboler som används för att representera det markerade/omarkerade tillståndet för en innehållskontroll i kryssrutan.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttag/)
* hopsättning [Aspose.Words](../../../)


