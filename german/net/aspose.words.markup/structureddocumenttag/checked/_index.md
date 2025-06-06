---
title: StructuredDocumentTag.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words für .NET
description: Verwalten Sie Checkbox-SDTs mit der Eigenschaft „StructuredDocumentTag Checked“. Der Status lässt sich einfach abrufen/festlegen – der Standardwert ist „false“. Verbessern Sie noch heute die Dokumentinteraktivität!
type: docs
weight: 60
url: /de/net/aspose.words.markup/structureddocumenttag/checked/
---
## StructuredDocumentTag.Checked property

Ruft den aktuellen Status des Kontrollkästchens ab/setzt ihn**SDT** . Der Standardwert für diese Eigenschaft ist`FALSCH` .

```csharp
public bool Checked { get; set; }
```

## Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürCheckbox SDT-Typen.

Bei allen anderen SDT-Typen tritt eine Ausnahme auf.

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

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
