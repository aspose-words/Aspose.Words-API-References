---
title: Enum TableAlignment
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Tables.TableAlignment opsomming. Gibt die Ausrichtung für eine InlineTabelle an.
type: docs
weight: 6050
url: /de/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Gibt die Ausrichtung für eine Inline-Tabelle an.

```csharp
public enum TableAlignment
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Left | `0` | Die Tabelle wird links ausgerichtet. |
| Center | `1` | Der Tisch wird zentriert. |
| Right | `2` | Die Tabelle wird rechtsbündig ausgerichtet. |

### Beispiele

Zeigt, wie Sie einen Gliederungsrahmen auf eine Tabelle anwenden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Richten Sie die Tabelle an der Mitte der Seite aus.
table.Alignment = TableAlignment.Center;

// Löschen Sie alle vorhandenen Rahmen und Schattierungen aus der Tabelle.
table.ClearBorders();
table.ClearShading();

// Fügen Sie dem Umriss der Tabelle grüne Ränder hinzu.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Füllen Sie die Zellen mit einer hellgrünen Volltonfarbe.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Tables](../../aspose.words.tables/)
* Montage [Aspose.Words](../../)


