---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Comparing.Granularity per tracciare con precisione e semplicità le modifiche ai documenti. Migliora il confronto dei tuoi documenti oggi stesso!
type: docs
weight: 490
url: /it/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

Specifica la granularità delle modifiche da monitorare quando si confrontano due documenti.

```csharp
public enum Granularity
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CharLevel | `0` | Specifica le modifiche a livello di carattere. |
| WordLevel | `1` | Specifica le modifiche a livello di parola. |

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

* spazio dei nomi [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assemblea [Aspose.Words](../../)
