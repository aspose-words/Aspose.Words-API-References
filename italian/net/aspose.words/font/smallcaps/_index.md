---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words per .NET
description: Font SmallCaps proprietà. Vero se il carattere è formattato come lettere maiuscole in C#.
type: docs
weight: 360
url: /it/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

Vero se il carattere è formattato come lettere maiuscole.

```csharp
public bool SmallCaps { get; set; }
```

## Esempi

Mostra come formattare un'esecuzione per visualizzarne il contenuto in maiuscolo.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Esistono due modi per far sì che un'esecuzione visualizzi il testo minuscolo in maiuscolo senza modificare il contenuto.
// 1 - Imposta il flag AllCaps per visualizzare tutti i caratteri in maiuscolo regolare:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Imposta il flag SmallCaps per visualizzare tutti i caratteri in maiuscoletto:
// Se un carattere è minuscolo, apparirà nella sua forma maiuscola
// ma avrà la stessa altezza delle lettere minuscole (l'altezza x del carattere).
// I caratteri che originariamente erano in maiuscolo appariranno uguali.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
