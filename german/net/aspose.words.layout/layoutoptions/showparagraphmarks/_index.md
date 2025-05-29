---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „LayoutOptions ShowParagraphMarks“ die Textformatierung durch Umschalten der Sichtbarkeit von Absatzmarken verbessert. Verbessern Sie noch heute die Übersichtlichkeit Ihres Dokuments!
type: docs
weight: 90
url: /de/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

Ruft ab oder legt fest, ob Absatzmarken gerendert werden. Der Standardwert ist`FALSCH` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## Beispiele

Zeigt, wie Absatzmarken in einem gerenderten Ausgabedokument angezeigt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Fügen Sie einige Absätze hinzu und aktivieren Sie dann Absatzmarken, um die Enden der Absätze anzuzeigen
// mit einem Absatzsymbol (¶), wenn wir das Dokument rendern.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### Siehe auch

* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
