---
title: ParagraphFormat.KeepWithNext
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Vero se il paragrafo deve rimanere nella stessa pagina del paragrafo successivo.
type: docs
weight: 160
url: /it/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

Vero se il paragrafo deve rimanere nella stessa pagina del paragrafo successivo.

```csharp
public bool KeepWithNext { get; set; }
```

### Esempi

Mostra come impostare un tavolo per stare insieme sulla stessa pagina.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Abilitazione KeepWithNext per ogni paragrafo della tabella ad eccezione di
// gli ultimi nell'ultima riga impediranno alla tabella di dividersi su più pagine.
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


