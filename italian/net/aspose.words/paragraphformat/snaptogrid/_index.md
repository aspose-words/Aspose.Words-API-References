---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words per .NET
description: Scopri come la proprietà ParagraphFormat SnapToGrid migliora la precisione del layout allineando i paragrafi alle linee della griglia del documento, per un aspetto più ordinato.
type: docs
weight: 300
url: /it/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Specifica se il paragrafo corrente deve utilizzare le impostazioni delle linee della griglia del documento per pagina quando si dispone il contenuto nel paragrafo.

```csharp
public bool SnapToGrid { get; set; }
```

## Esempi

Mostra come specificare un limite per il numero di righe che ogni pagina può contenere.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Abilita il pitching e poi usalo per impostare il numero di righe per pagina in questa sezione.
// Una dimensione del carattere sufficientemente grande sposterà alcune righe sulla pagina successiva per evitare la sovrapposizione di caratteri.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
