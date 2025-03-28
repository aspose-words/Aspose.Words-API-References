---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words for .NET
description: Discover the Font ComplexScript property, ensuring your text is formatted as complex script for enhanced readability and style, regardless of Unicode values.
type: docs
weight: 80
url: /net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Specifies whether the contents of this run shall be treated as complex script text regardless of their Unicode character values when determining the formatting for this run.

```csharp
public bool ComplexScript { get; set; }
```

## Examples

Shows how to add text that is always treated as complex script.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
