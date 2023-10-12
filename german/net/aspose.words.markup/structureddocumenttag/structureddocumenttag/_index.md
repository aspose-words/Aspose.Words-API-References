---
title: StructuredDocumentTag.StructuredDocumentTag
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag constructeur. Initialisiert eine neue Instanz von Strukturiertes DokumentTag Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Initialisiert eine neue Instanz von **Strukturiertes Dokument-Tag** Klasse.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| type | SdtType | Typ des SDT-Knotens. |
| level | MarkupLevel | Ebene des SDT-Knotens innerhalb des Dokuments. |

### Bemerkungen

Die folgenden Arten von SDT können erstellt werden:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

### Beispiele

Zeigen Sie, wie Sie ein strukturiertes Dokument-Tag in Form eines Kontrollkästchens erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Wir können die Symbole festlegen, die verwendet werden, um den aktivierten/nicht aktivierten Status eines Kontrollkästchen-Inhaltssteuerelements darzustellen.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Siehe auch

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [SdtType](../../sdttype/)
* enum [MarkupLevel](../../markuplevel/)
* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


