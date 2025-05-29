---
title: FindReplaceOptions.LegacyMode
linktitle: LegacyMode
articleTitle: LegacyMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà LegacyMode di FindReplaceOptions per attivare/disattivare facilmente l'algoritmo classico di ricerca/sostituzione, per funzionalità avanzate e un'esperienza utente fluida.
type: docs
weight: 130
url: /it/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

Ottiene o imposta un valore booleano che indica che viene utilizzato il vecchio algoritmo di ricerca/sostituzione.

```csharp
public bool LegacyMode { get; set; }
```

## Osservazioni

Utilizza questo flag se desideri esattamente lo stesso comportamento di prima dell'introduzione della funzionalità avanzata di ricerca/sostituzione. Tieni presente che il vecchio algoritmo non supporta funzionalità avanzate come la sostituzione con interruzioni, l'applicazione di formattazione e così via.

## Esempi

Mostra come riconoscere e utilizzare le sostituzioni all'interno dei modelli di sostituzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// L'utilizzo della modalità legacy non supporta molte funzionalità avanzate, quindi dobbiamo impostarla su "false".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### Guarda anche

* class [FindReplaceOptions](../)
* spazio dei nomi [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assemblea [Aspose.Words](../../../)
