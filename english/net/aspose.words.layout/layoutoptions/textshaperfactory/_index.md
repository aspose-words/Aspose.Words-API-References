---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words for .NET
description: Discover the LayoutOptions TextShaperFactory property for advanced typography. Enhance your rendering with customizable ITextShaperFactory implementations.
type: docs
weight: 100
url: /net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Gets or sets [`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) implementation used for Advanced Typography rendering features.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Examples

Shows how to support OpenType features using the HarfBuzz text shaping engine.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words can use externally provided text shaper objects,
// which represent fonts and compute shaping information for text.
// A text shaper factory is necessary for documents that use multiple fonts.
// When the text shaper factory set, the layout uses OpenType features.
// An Instance property returns a static BasicTextShaperCache object wrapping HarfBuzzTextShaperFactory.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Currently, text shaping is performing when exporting to PDF or XPS formats.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### See Also

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* namespace [Aspose.Words.Layout](../../../aspose.words.layout/)
* assembly [Aspose.Words](../../../)
