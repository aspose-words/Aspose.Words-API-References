---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words per .NET
description: Scopri la proprietà PhoneticGuide BaseText per accedere facilmente al testo base della guida fonetica e migliorarlo per una maggiore chiarezza e comunicazione.
type: docs
weight: 10
url: /it/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Ottiene il testo base della guida fonetica.

```csharp
public string BaseText { get; }
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

* class [PhoneticGuide](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
