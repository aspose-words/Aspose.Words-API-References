---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.PhoneticGuide per migliorare la leggibilità del testo con guide fonetiche. Migliora l'esperienza utente e l'accessibilità senza sforzo!
type: docs
weight: 5160
url: /it/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Rappresenta la guida fonetica.

```csharp
public class PhoneticGuide
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Ottiene il testo base della guida fonetica. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Ottiene il testo Ruby della guida fonetica. |

## Esempi

Mostra come ottenere le proprietà della guida fonetica.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utilizzare la guida fonetica nel testo asiatico.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
