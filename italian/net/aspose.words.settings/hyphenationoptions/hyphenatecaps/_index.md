---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words per .NET
description: HyphenationOptions HyphenateCaps proprietà. Ottiene o imposta un valore che determina se le parole scritte in maiuscolo sono sillabate. Il valore predefinito per questa proprietà èVERO  in C#.
type: docs
weight: 40
url: /it/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

Ottiene o imposta un valore che determina se le parole scritte in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è`VERO` .

```csharp
public bool HyphenateCaps { get; set; }
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

* class [HyphenationOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
