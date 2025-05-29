---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words per .NET
description: Scopri IsPhoneticGuide, un potente strumento che determina se una sequenza funge da guida fonetica, migliorando la chiarezza e la leggibilità del tuo testo.
type: docs
weight: 20
url: /it/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Ottiene un valore booleano che indica se la corsa è una guida fonetica.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
