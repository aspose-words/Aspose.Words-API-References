---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Drawing.VerticalAlignment für die präzise vertikale Ausrichtung von Textrahmen und Tabellen in Ihren Dokumenten. Verbessern Sie die Layoutkontrolle!
type: docs
weight: 1790
url: /de/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Gibt die vertikale Ausrichtung einer schwebenden Form, eines Textrahmens oder einer schwebenden Tabelle an.

```csharp
public enum VerticalAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Das Objekt wird explizit positioniert, normalerweise mithilfe seines**Spitze** Eigenschaft. |
| Top | `1` | Gibt an, dass sich das Objekt oben auf der vertikalen Ausrichtungsbasis befinden soll. |
| Center | `2` | Gibt an, dass das Objekt in Bezug auf die vertikale Ausrichtungsbasis zentriert werden soll. |
| Bottom | `3` | Gibt an, dass sich das Objekt am unteren Ende der vertikalen Ausrichtungsbasis befinden soll. |
| Inside | `4` | Gibt an, dass sich das Objekt innerhalb der horizontalen Ausrichtungsbasis befinden soll. |
| Outside | `5` | Gibt an, dass das Objekt außerhalb der vertikalen Ausrichtungsbasis liegen soll. |
| Inline | `-1` | Nicht dokumentiert. Scheint ein möglicher Wert für schwebende Absätze und Tabellen zu sein. |
| Default | `0` | Das Gleiche wieNone . |

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
