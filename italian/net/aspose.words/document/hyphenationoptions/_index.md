---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words per .NET
description: Esplora la proprietà Document HyphenationOptions per personalizzare le impostazioni di sillabazione, migliorando così la leggibilità e la presentazione del documento.
type: docs
weight: 220
url: /it/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

Fornisce accesso alle opzioni di sillabazione del documento.

```csharp
public HyphenationOptions HyphenationOptions { get; }
```

## Esempi

Mostra come configurare la sillabazione automatica.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### Guarda anche

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
