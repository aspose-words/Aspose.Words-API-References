---
title: LayoutOptions.ShowHiddenText
linktitle: ShowHiddenText
articleTitle: ShowHiddenText
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „LayoutOptions ShowHiddenText“ und steuern Sie ganz einfach die Darstellung von verstecktem Text in Ihren Dokumenten. Optimieren Sie noch heute die Sichtbarkeit Ihrer Inhalte!
type: docs
weight: 80
url: /de/net/aspose.words.layout/layoutoptions/showhiddentext/
---
## LayoutOptions.ShowHiddenText property

Ruft ab oder legt fest, ob versteckter Text im Dokument gerendert wird. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowHiddenText { get; set; }
```

## Bemerkungen

Diese Eigenschaft betrifft alle ausgeblendeten Inhalte, nicht nur Text.

## Beispiele

Zeigt, wie Text in einem gerenderten Ausgabedokument ausgeblendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Versteckten Text einfügen und dann angeben, ob er aus einem gerenderten Dokument weggelassen werden soll.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

### Siehe auch

* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
