---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words per .NET
description: Scopri la proprietà Granularità di CompareOptions, traccia le modifiche per carattere o parola per una modifica precisa del testo. Migliora il controllo dei tuoi documenti oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Specifica se le modifiche vengono tracciate per carattere o per parola.

```csharp
public Granularity Granularity { get; set; }
```

## Osservazioni

Il valore predefinito èWordLevel .

## Esempi

Mostra come specificare una granularità durante il confronto dei documenti.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specificare se le modifiche vengono monitorate
// per carattere ('Granularity.CharLevel') o per parola ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La raccolta di gruppi di revisione del primo documento contiene tutte le differenze tra i documenti.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Guarda anche

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* spazio dei nomi [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../../)
