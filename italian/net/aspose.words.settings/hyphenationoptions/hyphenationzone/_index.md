---
title: HyphenationOptions.HyphenationZone
second_title: Aspose.Words per .NET API Reference
description: HyphenationOptions proprietà. Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro il quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 025 pollici.
type: docs
weight: 50
url: /it/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro il quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollici).

```csharp
public int HyphenationZone { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words.Settings](../../hyphenationoptions/)
* assemblea [Aspose.Words](../../../)


