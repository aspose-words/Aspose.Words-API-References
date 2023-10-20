---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words für .NET
description: ParagraphFormat LinesToDrop eigendom. Ruft die Anzahl der Zeilen des Absatztextes ab der zur Berechnung der Initialenhöhe verwendet wird oder legt diese fest in C#.
type: docs
weight: 210
url: /de/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Ruft die Anzahl der Zeilen des Absatztextes ab, der zur Berechnung der Initialenhöhe verwendet wird, oder legt diese fest.

```csharp
public int LinesToDrop { get; set; }
```

## Beispiele

Zeigt, wie die Größe einer Initiale festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändern Sie die Eigenschaft „LinesToDrop“, um einen Absatz als Initiale festzulegen.
// wodurch daraus ein großer Großbuchstabe wird, der den nächsten Absatz schmückt.
// Geben Sie dieser Eigenschaft den Wert 4, um der Initiale die Höhe von vier Textzeilen zu geben.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Setzen Sie die Eigenschaft „LinesToDrop“ auf 0 zurück, um den nächsten Absatz in einen normalen Absatz umzuwandeln.
// Der Text in diesem Absatz wird um die Initiale umbrochen.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
