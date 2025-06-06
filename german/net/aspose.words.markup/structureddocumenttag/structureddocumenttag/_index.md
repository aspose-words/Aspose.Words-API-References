---
title: StructuredDocumentTag
linktitle: StructuredDocumentTag
articleTitle: StructuredDocumentTag
second_title: Aspose.Words für .NET
description: Erstellen Sie mühelos leistungsstarke strukturierte Dokumente mit dem StructuredDocumentTag-Konstruktor. Initialisieren Sie neue Instanzen für mehr Übersichtlichkeit und Übersichtlichkeit.
type: docs
weight: 10
url: /de/net/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag constructor

Initialisiert eine neue Instanz des**Strukturiertes Dokument-Tag** Klasse.

```csharp
public StructuredDocumentTag(DocumentBase doc, SdtType type, MarkupLevel level)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | DocumentBase | Das Eigentümerdokument. |
| type | SdtType | Typ des SDT-Knotens. |
| level | MarkupLevel | Ebene des SDT-Knotens innerhalb des Dokuments. |

## Bemerkungen

Die folgenden SDT-Typen können erstellt werden:

* Checkbox
* DropDownList
* ComboBox
* Date
* BuildingBlockGallery
* Group
* Picture
* RichText
* PlainText

## Beispiele

Zeigen Sie, wie Sie ein strukturiertes Dokument-Tag in Form eines Kontrollkästchens erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

StructuredDocumentTag sdtCheckBox =
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) { Checked = true };

// Wir können die Symbole festlegen, die zur Darstellung des aktivierten/deaktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet werden.
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
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
