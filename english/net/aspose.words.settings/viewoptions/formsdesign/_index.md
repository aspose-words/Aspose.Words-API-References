---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words for .NET
description: Discover how ViewOptions FormsDesign enhances your document experience by toggling forms design mode for seamless editing and customization.
type: docs
weight: 30
url: /net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Specifies whether the document is in forms design mode.

```csharp
public bool FormsDesign { get; set; }
```

## Remarks

Currently works only for documents in WordML format.

## Examples

Shows how to enable/disable forms design mode.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Set the "FormsDesign" property to "false" to keep forms design mode disabled.
// Set the "FormsDesign" property to "true" to enable forms design mode.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### See Also

* class [ViewOptions](../)
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
