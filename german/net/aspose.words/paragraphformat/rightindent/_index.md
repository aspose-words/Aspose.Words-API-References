---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie den rechten Einzug Ihrer Absätze mit der ParagraphFormat RightIndent-Eigenschaft ganz einfach anpassen. Optimieren Sie noch heute die Formatierung Ihrer Dokumente!
type: docs
weight: 280
url: /de/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

Ruft den Wert (in Punkten) ab oder legt ihn fest, der den rechten Einzug für den Absatz darstellt.

```csharp
public double RightIndent { get; set; }
```

## Beispiele

Zeigt, wie Sie die Absatzformatierung konfigurieren, um außermittigen Text zu erstellen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Zentrieren Sie den gesamten Text, den der Dokumentgenerator schreibt, und richten Sie Einrückungen ein.
// Die folgende Einzugskonfiguration erstellt einen Textkörper, der asymmetrisch auf der Seite angeordnet ist.
// Die „Mitte“, an der wir den Text ausrichten, ist die Mitte des Textkörpers, nicht die Mitte der Seite.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
