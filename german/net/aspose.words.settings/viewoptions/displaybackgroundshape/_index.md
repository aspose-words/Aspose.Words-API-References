---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „DisplayBackgroundShape“ in „ViewOptions“, um Ihr Drucklayout mit anpassbaren Hintergrundformen für ein elegantes Erscheinungsbild zu verbessern.
type: docs
weight: 10
url: /de/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Beispiele

Zeigt, wie Hintergrundbilder von Dokumenten in den Ansichtsoptionen ausgeblendet/angezeigt werden.

```csharp
// Verwenden Sie eine HTML-Zeichenfolge, um ein neues Dokument mit einer flachen Hintergrundfarbe zu erstellen.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Die Quelle für das Dokument hat einen flachen Farbhintergrund,
// dessen Vorhandensein das Flag „DisplayBackgroundShape“ auf „true“ setzt.
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Behalten Sie „DisplayBackgroundShape“ auf „true“, damit das Dokument die Hintergrundfarbe anzeigt.
// Dies kann einige Textfarben beeinflussen, um die Sichtbarkeit zu verbessern.
// Setzen Sie „DisplayBackgroundShape“ auf „false“, um die Hintergrundfarbe nicht anzuzeigen.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
