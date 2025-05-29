---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words für .NET
description: Entdecken Sie die Unterstreichungsfunktion von DocumentBuilder, um Schriftstile einfach anzupassen. Optimieren Sie Ihre Dokumente mit vielseitigen Unterstreichungsoptionen für ein professionelles Erscheinungsbild.
type: docs
weight: 190
url: /de/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Ruft den Unterstreichungstyp für die aktuelle Schriftart ab/legt ihn fest.

```csharp
public Underline Underline { get; set; }
```

## Beispiele

Zeigt, wie von einem Dokumentgenerator eingefügter Text formatiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Der Builder wendet die Formatierung auf den aktuellen Absatz und allen neuen Text an, der danach hinzugefügt wird.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Siehe auch

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
