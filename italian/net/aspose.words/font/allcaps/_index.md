---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font AllCaps. Formatta facilmente il testo in maiuscolo per una migliore leggibilità e un design d'impatto nei tuoi progetti.
type: docs
weight: 10
url: /it/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Vero se il font è formattato con tutte lettere maiuscole.

```csharp
public bool AllCaps { get; set; }
```

## Esempi

Mostra come formattare una serie per visualizzarne il contenuto in maiuscolo.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Esistono due modi per far sì che un'esecuzione visualizzi il suo testo in minuscolo in maiuscolo senza modificarne il contenuto.
// 1 - Imposta il flag AllCaps per visualizzare tutti i caratteri in maiuscolo:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Imposta il flag SmallCaps per visualizzare tutti i caratteri in maiuscolo piccolo:
// Se un carattere è minuscolo, apparirà nella sua forma maiuscola
// ma avrà la stessa altezza della lettera minuscola (l'altezza x del font).
// I caratteri che originariamente erano in maiuscolo avranno lo stesso aspetto.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
