---
title: Run.PhoneticGuide
second_title: Aspose.Words per .NET API Reference
description: Run proprietà. Ottiene aPhoneticGuide oggetto.
type: docs
weight: 40
url: /it/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Ottiene a`PhoneticGuide` oggetto.

```csharp
public PhoneticGuide PhoneticGuide { get; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../run/)
* assemblea [Aspose.Words](../../../)


