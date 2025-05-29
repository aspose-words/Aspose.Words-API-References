---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Tables.TableAlignment für eine optimale Inline-Tabellenausrichtung. Verbessern Sie die Formatierung Ihres Dokuments präzise und einfach.
type: docs
weight: 7200
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
| Left | `0` | Die Tabelle ist linksbündig ausgerichtet. |
| Center | `1` | Die Tabelle ist zentriert. |
| Right | `2` | Die Tabelle ist rechtsbündig ausgerichtet. |

## Beispiele

Zeigt, wie Sie einer Tabelle einen Gliederungsrahmen hinzufügen.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Richten Sie die Tabelle an der Seitenmitte aus.
table.Alignment = TableAlignment.Center;

// Alle vorhandenen Ränder und Schattierungen aus der Tabelle löschen.
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
