---
title: Font.AllCaps
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Vero se il carattere è formattato con tutte lettere maiuscole.
type: docs
weight: 10
url: /it/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Vero se il carattere è formattato con tutte lettere maiuscole.

```csharp
public bool AllCaps { get; set; }
```

### Esempi

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
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


