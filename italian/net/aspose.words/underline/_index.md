---
title: Underline Enum
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Underline per opzioni versatili di sottolineatura dei font. Migliora la formattazione dei tuoi documenti con stili personalizzabili oggi stesso!
type: docs
weight: 7360
url: /it/net/aspose.words/underline/
---
## Underline enumeration

Indica il tipo di sottolineatura applicata a un font.

```csharp
public enum Underline
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` |  |
| Single | `1` |  |
| Words | `2` |  |
| Double | `3` |  |
| Dotted | `4` |  |
| Thick | `6` |  |
| Dash | `7` |  |
| DashLong | `39` |  |
| DotDash | `9` |  |
| DotDotDash | `10` |  |
| Wavy | `11` |  |
| DottedHeavy | `20` |  |
| DashHeavy | `23` |  |
| DashLongHeavy | `55` |  |
| DotDashHeavy | `25` |  |
| DotDotDashHeavy | `26` |  |
| WavyHeavy | `27` |  |
| WavyDouble | `43` |  |

## Esempi

Mostra come inserire un campo collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserisci un collegamento ipertestuale ed evidenzialo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Facendo clic con il tasto sinistro del mouse sul collegamento nel testo in Microsoft Word verremo indirizzati all'URL tramite una nuova finestra del browser Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
