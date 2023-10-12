---
title: LayoutOptions.ShowHiddenText
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutOptions eigendom. Ruft den Hinweis ab ob versteckter Text im Dokument gerendert wird oder legt diesen fest. Standard istFALSCH .
type: docs
weight: 80
url: /de/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Ruft den Hinweis ab, ob versteckter Text im Dokument gerendert wird, oder legt diesen fest. Standard ist`FALSCH` .

```csharp
public bool ShowHiddenText { get; set; }
```

### Bemerkungen

Diese Eigenschaft betrifft alle ausgeblendeten Inhalte, nicht nur Text.

### Beispiele

Zeigt, wie Text in einem gerenderten Ausgabedokument ausgeblendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Versteckten Text einfügen und dann angeben, ob wir ihn in einem gerenderten Dokument weglassen möchten.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Siehe auch

* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../layoutoptions/)
* Montage [Aspose.Words](../../../)


