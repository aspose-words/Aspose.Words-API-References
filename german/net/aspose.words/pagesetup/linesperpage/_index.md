---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words für .NET
description: Steuern Sie Ihr Dokumentlayout mit der Eigenschaft „PageSetup LinesPerPage“. Passen Sie die Zeilen pro Seite einfach an, um optimale Lesbarkeit und Organisation zu gewährleisten.
type: docs
weight: 240
url: /de/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Ruft die Anzahl der Zeilen pro Seite im Dokumentraster ab oder legt sie fest.

```csharp
public int LinesPerPage { get; set; }
```

## Bemerkungen

Der Mindestwert der Eigenschaft ist 1. Der Maximalwert hängt von der Seitenhöhe und der Schriftgröße des Stils „Normal“ ab. Der minimale Zeilenabstand beträgt 136 Prozent der Schriftgröße. Beispielsweise beträgt die maximale Zeilenanzahl pro Seite einer Letter-Seite mit 2,5 cm Rand 39.

Standardmäßig hat die Eigenschaft einen Wert, bei dem der Zeilenabstand 1,5-mal größer ist als die Schriftgröße von im Stil „Normal“.

## Beispiele

Zeigt, wie Sie eine Begrenzung für die Zeilenanzahl festlegen, die jede Seite haben darf.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Pitching aktivieren und dann damit die Zeilenanzahl pro Seite in diesem Abschnitt festlegen.
// Eine ausreichend große Schriftgröße verschiebt einige Zeilen auf die nächste Seite, um überlappende Zeichen zu vermeiden.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
