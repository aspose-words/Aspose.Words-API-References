---
title: ViewOptions.DisplayBackgroundShape
second_title: Aspose.Words für .NET-API-Referenz
description: ViewOptions eigendom. Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht.
type: docs
weight: 10
url: /de/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Steuert die Anzeige der Hintergrundform in der Drucklayoutansicht.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### Beispiele

Zeigt, wie Hintergrundbilder von Dokumenten in Ansichtsoptionen ausgeblendet/angezeigt werden.

```csharp
// Verwenden Sie einen HTML-String, um ein neues Dokument mit einer flachen Hintergrundfarbe zu erstellen.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// Die Quelle für das Dokument hat einen flachen Farbhintergrund,
// dessen Vorhandensein setzt das "DisplayBackgroundShape"-Flag auf "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// "DisplayBackgroundShape" auf "true" belassen, damit das Dokument die Hintergrundfarbe anzeigt.
// Dies kann sich auf einige Textfarben auswirken, um die Sichtbarkeit zu verbessern.
// Setzen Sie "DisplayBackgroundShape" auf "false", um die Hintergrundfarbe nicht anzuzeigen.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../viewoptions/)
* Montage [Aspose.Words](../../../)


