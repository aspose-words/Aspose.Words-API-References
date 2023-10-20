---
title: StructuredDocumentTag.SetCheckedSymbol
linktitle: SetCheckedSymbol
articleTitle: SetCheckedSymbol
second_title: Aspose.Words für .NET
description: StructuredDocumentTag SetCheckedSymbol methode. Legt das Symbol fest das zur Darstellung des aktivierten Status eines KontrollkästchenInhaltssteuerelements verwendet wird in C#.
type: docs
weight: 360
url: /de/net/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag.SetCheckedSymbol method

Legt das Symbol fest, das zur Darstellung des aktivierten Status eines Kontrollkästchen-Inhaltssteuerelements verwendet wird.

```csharp
public void SetCheckedSymbol(int characterCode, string fontName)
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
    new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline) {Checked = true};

// Wir können die Symbole festlegen, die verwendet werden, um den aktivierten/nicht aktivierten Status eines Kontrollkästchen-Inhaltssteuerelements darzustellen.
sdtCheckBox.SetCheckedSymbol(0x00A9, "Times New Roman");
sdtCheckBox.SetUncheckedSymbol(0x00AE, "Times New Roman");

builder.InsertNode(sdtCheckBox);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CheckBox.docx");
```

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
