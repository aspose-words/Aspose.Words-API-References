---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.HorizontalAlignment für präzise Kontrolle der horizontalen Ausrichtung in schwebenden Textrahmen und Tabellen. Verbessern Sie Ihr Dokumentlayout!
type: docs
weight: 1360
url: /de/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Gibt die horizontale Ausrichtung einer schwebenden Form, eines Textrahmens oder einer schwebenden Tabelle an.

```csharp
public enum HorizontalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Das Objekt wird explizit positioniert, normalerweise mithilfe seines**Links** Eigenschaft. |
| Default | `0` | Das Gleiche wieNone . |
| Left | `1` | Gibt an, dass das Objekt linksbündig an der horizontalen Ausrichtungsbasis ausgerichtet werden soll. |
| Center | `2` | Gibt an, dass das Objekt in Bezug auf die horizontale Ausrichtungsbasis zentriert werden soll. |
| Right | `3` | Gibt an, dass das Objekt rechtsbündig an der horizontalen Ausrichtungsbasis ausgerichtet werden soll. |
| Inside | `4` | Gibt an, dass sich das Objekt innerhalb der horizontalen Ausrichtungsbasis befinden soll. |
| Outside | `5` | Gibt an, dass das Objekt außerhalb der horizontalen Ausrichtungsbasis liegen soll. |

## Beispiele

Zeigt, wie ein schwebendes Bild in die Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Seitenmitte aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Siehe auch

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
