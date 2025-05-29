---
title: SectionCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a sezioni specifiche con la proprietà SectionCollection Item. Recupera qualsiasi sezione tramite indice per una gestione semplificata dei dati.
type: docs
weight: 10
url: /it/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Recupera una sezione all'indice specificato.

```csharp
public Section this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nell'elenco delle sezioni. |

## Osservazioni

L'indice è basato sullo zero.

Sono consentiti indici negativi che indicano l'accesso dalla parte posteriore della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, viene restituito un riferimento null.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, viene restituito un riferimento null.

## Esempi

Indica quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta verranno eseguiti automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificare il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Nella versione corrente di Aspose.Words, la modifica del documento non ne comporta la ricostruzione automatica
// il layout della pagina memorizzato nella cache. Se desideriamo il layout memorizzato nella cache
// Per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Mostra come preparare un nuovo nodo di sezione per la modifica.

```csharp
Document doc = new Document();

// Un documento vuoto è composto da una sezione, che a sua volta ha un corpo, che a sua volta ha un paragrafo.
// Possiamo aggiungere contenuti a questo documento inserendo elementi come sequenze di testo, forme o tabelle nel paragrafo.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Se aggiungiamo una nuova sezione come questa, non avrà un corpo né altri nodi figlio.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Esegui il metodo "EnsureMinimum" per aggiungere un corpo e un paragrafo a questa sezione per iniziare a modificarla.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [Section](../../section/)
* class [SectionCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
