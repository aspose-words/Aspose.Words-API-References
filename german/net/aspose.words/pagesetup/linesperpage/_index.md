---
title: PageSetup.LinesPerPage
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Ruft die Anzahl der Zeilen pro Seite im Dokumentraster ab oder legt sie fest.
type: docs
weight: 240
url: /de/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Ruft die Anzahl der Zeilen pro Seite im Dokumentraster ab oder legt sie fest.

```csharp
public int LinesPerPage { get; set; }
```

### Bemerkungen

Der Mindestwert der Eigenschaft ist 1. Der Höchstwert hängt von der Seitenhöhe und der Schriftgröße des Stils Normal ab. Der minimale Zeilenabstand beträgt 136 Prozent der Schriftgröße. Beispielsweise beträgt die maximale Zeilenzahl pro Seite einer Letter-Seite mit 1-Zoll-Rändern 39.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeilenabstand 1,5-mal größer ist als die Schriftgröße von des Stils Normal.

### Beispiele

Zeigt, wie Sie ein Limit für die Anzahl der Zeilen angeben, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aktivieren Sie Pitching und verwenden Sie es dann, um die Anzahl der Zeilen pro Seite in diesem Abschnitt festzulegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen nach unten auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


