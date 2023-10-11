---
title: Enum Granularity
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Comparing.Granularity enum. Specifica la granularità delle modifiche da tenere traccia quando si confrontano due documenti.
type: docs
weight: 290
url: /it/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Specifica la granularità delle modifiche da tenere traccia quando si confrontano due documenti.

```csharp
public enum Granularity
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

### Esempi

Mostra per specificare una granularità durante il confronto dei documenti.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Specifica se le modifiche vengono monitorate
// per carattere ('Granularity.CharLevel') o per parola ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La raccolta di gruppi di revisione del primo documento contiene tutte le differenze tra i documenti.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../)


