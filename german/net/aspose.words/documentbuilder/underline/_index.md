---
title: DocumentBuilder.Underline
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. Ruft den Unterstreichungstyp für die aktuelle Schriftart ab bzw. legt diesen fest.
type: docs
weight: 190
url: /de/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Ruft den Unterstreichungstyp für die aktuelle Schriftart ab bzw. legt diesen fest.

```csharp
public Underline Underline { get; set; }
```

### Beispiele

Zeigt, wie von einem Dokumentersteller eingefügter Text formatiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Der Builder wendet die Formatierung auf seinen aktuellen Absatz und jeden neuen Text an, der danach hinzugefügt wird.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Siehe auch

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


