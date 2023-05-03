---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words for .NET API Reference
description: ViewOptions DisplayBackgroundShape property. Controls display of the background shape in print layout view in C#.
type: docs
weight: 10
url: /net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

Controls display of the background shape in print layout view.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## Examples

Shows how to hide/display document background images in view options.

```csharp
// Use an HTML string to create a new document with a flat background color.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// The source for the document has a flat color background,
// the presence of which will set the "DisplayBackgroundShape" flag to "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// Keep the "DisplayBackgroundShape" as "true" to get the document to display the background color.
// This may affect some text colors to improve visibility.
// Set the "DisplayBackgroundShape" to "false" to not display the background color.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### See Also

* class [ViewOptions](../)
* namespace [Aspose.Words.Settings](../../viewoptions/)
* assembly [Aspose.Words](../../../)
