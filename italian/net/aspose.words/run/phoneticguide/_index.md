---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words per .NET
description: Run PhoneticGuide proprietà. Ottiene aPhoneticGuide oggetto in C#.
type: docs
weight: 40
url: /it/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Ottiene a`PhoneticGuide` oggetto.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
