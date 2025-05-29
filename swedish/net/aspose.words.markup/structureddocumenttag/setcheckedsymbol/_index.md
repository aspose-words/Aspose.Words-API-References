---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words för .NET
description: Upptäck hur du använder metoden SetCheckedSymbol i StructuredDocumentTag för att anpassa kryssrutornas visuella element och förbättra användarupplevelsen.
type: docs
weight: 380
url: /sv/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Anger symbolen som används för att representera det markerade tillståndet för en innehållskontroll för kryssrutor.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| characterCode | Int32 | Teckenkoden för den angivna symbolen. |
| fontName | String | Namnet på teckensnittet som innehåller symbolen. |

## Anmärkningar

Åtkomst till den här metoden fungerar bara förCheckbox SDT-typer.

För alla andra SDT-typer kommer undantag att inträffa.

## Exempel

Visa hur man skapar en strukturerad dokumenttagg i form av en kryssruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Vi kan ställa in symbolerna som används för att representera det markerade/omarkerade tillståndet för en innehållskontroll för kryssrutan.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
