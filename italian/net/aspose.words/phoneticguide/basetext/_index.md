---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words per .NET
description: PhoneticGuide BaseText proprietà. Ottiene il testo di base della guida fonetica in C#.
type: docs
weight: 10
url: /it/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Ottiene il testo di base della guida fonetica.

```csharp
public string BaseText { get; }
```

## Esempi

Mostra come ottenere le proprietà della guida fonetica.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utilizza la guida fonetica nel testo asiatico.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Guarda anche

* class [PhoneticGuide](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
