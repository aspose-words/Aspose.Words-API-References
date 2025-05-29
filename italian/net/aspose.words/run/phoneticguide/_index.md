---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words per .NET
description: Ottieni una pronuncia impeccabile con PhoneticGuide. Migliora le tue competenze linguistiche e comunicative accedendo ad approfondimenti fonetici personalizzati.
type: docs
weight: 40
url: /it/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Ottiene un`PhoneticGuide` oggetto.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
