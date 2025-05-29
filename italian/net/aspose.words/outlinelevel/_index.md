---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.OutlineLevel per gestire facilmente i livelli di struttura dei paragrafi nei tuoi documenti, per una maggiore organizzazione e chiarezza.
type: docs
weight: 5060
url: /it/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Specifica il livello di struttura di un paragrafo nel documento.

```csharp
public enum OutlineLevel
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Level1 | `0` | Il paragrafo è al livello 1 dello schema (livello più alto). |
| Level2 | `1` | Il paragrafo è al livello 2 dello schema. |
| Level3 | `2` | Il paragrafo è al livello 3 dello schema. |
| Level4 | `3` | Il paragrafo è al livello 4 dello schema. |
| Level5 | `4` | Il paragrafo è al livello 5 dello schema. |
| Level6 | `5` | Il paragrafo è al livello di struttura 6. |
| Level7 | `6` | Il paragrafo è al livello 7 dello schema. |
| Level8 | `7` | Il paragrafo è al livello 8. |
| Level9 | `8` | Il paragrafo è al livello 9. |
| BodyText | `9` | Il paragrafo è al livello del testo principale. |

## Esempi

Mostra come configurare i livelli di struttura del paragrafo per creare testo comprimibile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni paragrafo ha un OutlineLevel, che può essere un numero compreso tra 1 e 9 oppure il valore predefinito "BodyText".
// Impostando la proprietà su uno dei valori numerati verrà visualizzata una freccia a sinistra
// dell'inizio del paragrafo.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Il livello 1 è il livello più alto. Se c'è un paragrafo con un livello inferiore al di sotto di un paragrafo con un livello superiore,
// la compressione del paragrafo di livello superiore comporterà la compressione del paragrafo di livello inferiore.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Due paragrafi dello stesso livello non si contrarranno a vicenda,
// e le frecce non comprimono i paragrafi a cui puntano.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// Il valore predefinito "BodyText" è il più basso che un paragrafo di qualsiasi livello può comprimere.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
