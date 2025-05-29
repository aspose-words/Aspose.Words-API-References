---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà OutlineLevel di ParagraphFormat per definire facilmente la gerarchia dei paragrafi nei tuoi documenti, migliorando l'organizzazione e la leggibilità.
type: docs
weight: 260
url: /it/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

Specifica il livello di struttura del paragrafo nel documento.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

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

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
