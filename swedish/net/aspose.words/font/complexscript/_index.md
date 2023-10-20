---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words för .NET
description: Font ComplexScript fast egendom. Anger om innehållet i denna körning ska behandlas som komplex skripttext oavsett deras Unicodeteckenvärden när formateringen för denna körning bestäms i C#.
type: docs
weight: 80
url: /sv/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Anger om innehållet i denna körning ska behandlas som komplex skripttext oavsett deras Unicode-teckenvärden när formateringen för denna körning bestäms.

```csharp
public bool ComplexScript { get; set; }
```

## Exempel

Visar hur man lägger till text som alltid behandlas som komplext skript.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Se även

* class [Font](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
