---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words per .NET
description: Scopri Font NoProofing. Impedisci il controllo ortografico sul testo formattato per un design più pulito. Migliora i tuoi documenti con precisione e professionalità!
type: docs
weight: 280
url: /it/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

Vero quando non si desidera controllare l'ortografia dei caratteri formattati.

```csharp
public bool NoProofing { get; set; }
```

## Esempi

Mostra come impedire il controllo ortografico del testo da parte di Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di solito, Microsoft Word evidenzia gli errori di ortografia con una sottolineatura rossa frastagliata.
// Possiamo deselezionare il flag "NoProofing" per creare una porzione di testo che
// ignora il controllo ortografico disattivandolo completamente.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
