---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font NumberSpacing-Eigenschaft, um den Ziffernabstand für bessere Lesbarkeit und Design anzupassen. Optimieren Sie Ihre Typografie noch heute!
type: docs
weight: 290
url: /de/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Ruft den Abstandstyp der angezeigten Ziffer ab oder legt ihn fest.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Beispiele

Zeigt, wie der Abstandstyp der Ziffer eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dieser Effekt wird nur in neueren Versionen von MS Word unterstützt.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Siehe auch

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
