---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words per .NET
description: Aspose.Words.Settings.HyphenationOptions classe. Permette di configurare le opzioni di sillabazione del documento in C#.
type: docs
weight: 5790
url: /it/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

Permette di configurare le opzioni di sillabazione del documento.

Per saperne di più, visita il[Lavorare con la sillabazione](https://docs.aspose.com/words/net/working-with-hyphenation/) articolo di documentazione.

```csharp
public class HyphenationOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | Ottiene o imposta un valore che determina se la sillabazione automatica è attivata per il documento. Il valore predefinito per questa proprietà è`falso` . |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | Ottiene o imposta il numero massimo di righe consecutive che possono terminare con trattini. Il valore predefinito per questa proprietà è 0. |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | Ottiene o imposta un valore che determina se le parole scritte in maiuscolo sono sillabate. Il valore predefinito per questa proprietà è`VERO` . |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | Ottiene o imposta la distanza in 1/20 di punto dal margine destro entro il quale non si desidera sillabare le parole. Il valore predefinito per questa proprietà è 360 (0,25 pollici). |

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

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
