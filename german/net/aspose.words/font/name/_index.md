---
title: Name
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft den Namen der Schriftart ab oder legt ihn fest.
type: docs
weight: 230
url: /de/net/aspose.words/font/name/
---
## Font.Name property

Ruft den Namen der Schriftart ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

### Bemerkungen

Wenn Sie kommen, kehrt zurück[`NameAscii`](../nameascii).

Beim Setzen setzt[`NameAscii`](../nameascii) ,[`NameBi`](../namebi) ,[`NameFarEast`](../namefareast) und[`NameOther`](../nameother) auf den angegebenen Wert.

### Beispiele

Zeigt, wie ein Textverlauf mithilfe seiner Eigenschaft font formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schriftartformatierung angeben, dann Text hinzufügen.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Siehe auch

* class [Font](../../font)
* namensraum [Aspose.Words](../../font)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->