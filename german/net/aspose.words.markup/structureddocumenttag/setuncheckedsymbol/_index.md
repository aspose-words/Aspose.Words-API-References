---
title: StructuredDocumentTag.SetUncheckedSymbol
linktitle: SetUncheckedSymbol
articleTitle: SetUncheckedSymbol
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode SetUncheckedSymbol Ihr StructuredDocumentTag verbessert, indem sie die visuelle Darstellung von Kontrollkästchen für eine bessere Benutzererfahrung anpasst.
type: docs
weight: 390
url: /de/net/aspose.words.markup/structureddocumenttag/setuncheckedsymbol/
---
## StructuredDocumentTag.SetUncheckedSymbol method

Legt das Symbol fest, das zur Darstellung des deaktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet wird.

```csharp
public void SetUncheckedSymbol(int characterCode, string fontName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| characterCode | Int32 | Der Zeichencode für das angegebene Symbol. |
| fontName | String | Der Name der Schriftart, die das Symbol enthält. |

## Bemerkungen

Der Zugriff auf diese Methode funktioniert nur fürCheckbox SDT-Typen.

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
