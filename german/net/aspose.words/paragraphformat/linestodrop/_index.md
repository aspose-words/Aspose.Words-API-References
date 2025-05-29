---
title: ParagraphFormat.LinesToDrop
linktitle: LinesToDrop
articleTitle: LinesToDrop
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „ParagraphFormat LinesToDrop“ die Initialenhöhe in Ihren Dokumenten verbessert. Optimieren Sie Ihr Textlayout für beeindruckende Grafiken!
type: docs
weight: 210
url: /de/net/aspose.words/paragraphformat/linestodrop/
---
## ParagraphFormat.LinesToDrop property

Ruft die Zeilenanzahl des Absatztexts ab oder legt sie fest, die zur Berechnung der Initialhöhe verwendet wird.

```csharp
public int LinesToDrop { get; set; }
```

## Beispiele

Zeigt, wie die Größe eines Initials festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ändern Sie die Eigenschaft „LinesToDrop“, um einen Absatz als Initiale zu kennzeichnen.
// Dadurch wird es in einen großen Großbuchstaben umgewandelt, der den nächsten Absatz schmückt.
// Geben Sie dieser Eigenschaft den Wert 4, um dem Initial die Höhe von vier Textzeilen zu geben.
builder.ParagraphFormat.LinesToDrop = 4;
builder.Writeln("H");

// Setzen Sie die Eigenschaft „LinesToDrop“ auf 0 zurück, um den nächsten Absatz in einen normalen Absatz umzuwandeln.
// Der Text in diesem Absatz wird um die Initiale herum umbrochen.
builder.ParagraphFormat.LinesToDrop = 0;
builder.Writeln("ello world!");

doc.Save(ArtifactsDir + "ParagraphFormat.LinesToDrop.odt");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
