---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.FillType, um Ihre ausfüllbaren Objekte mit vielseitigen Fülltypen für ein verbessertes Dokumentdesign zu erweitern.
type: docs
weight: 1280
url: /de/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Gibt den Fülltyp für ein ausfüllbares Objekt an.

```csharp
public enum FillType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Solid | `1` | Feste Füllung. |
| Patterned | `2` | Gemusterte Füllung. |
| Gradient | `3` | Verlaufsfüllung. |
| Textured | `4` | Strukturierte Füllung. |
| Background | `5` | Die Füllung ist die gleiche wie der Hintergrund. |
| Picture | `6` | Bildfüllung. |

## Beispiele

Zeigt, wie Sie beliebige Füllungen wieder in Vollfüllungen umwandeln.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Füllobjekt für die Schriftart des ersten Laufs abrufen.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Fülleigenschaften der Schriftart prüfen.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Ändern Sie den Füllungstyp in „Einfarbig“ mit einheitlicher grüner Farbe.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
