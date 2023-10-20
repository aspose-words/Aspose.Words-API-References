---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words för .NET
description: StructuredDocumentTag Checked fast egendom. Hämtar/ställer in aktuell status för kryssrutanSDT . Standardvärdet för den här egenskapen ärfalsk  i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Hämtar/ställer in aktuell status för kryssrutan**SDT** . Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool Checked { get; set; }
```

## Anmärkningar

Åtkomst till den här egenskapen fungerar bara förCheckbox SDT-typer.

För alla andra SDT-typer kommer undantag att förekomma.

## Exempel

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
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
