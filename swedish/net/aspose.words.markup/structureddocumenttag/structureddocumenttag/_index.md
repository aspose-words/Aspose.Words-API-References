---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words för .NET
description: Skapa kraftfulla strukturerade dokument utan ansträngning med konstruktorn StructuredDocumentTag. Initiera nya instanser för förbättrad organisation och tydlighet.
type: docs
weight: 10
url: /sv/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Initierar en ny instans av**Tagg för strukturerat dokument** klass.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | DocumentBase | Ägardokumentet. |
| type | SdtType | Typ av SDT-nod. |
| level | MarkupLevel | Nivå för SDT-nod i dokumentet. |

## Anmärkningar

Följande typer av SDT kan skapas:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

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

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
