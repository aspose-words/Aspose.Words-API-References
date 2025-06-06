---
title: ControlChar.FieldSeparatorChar
linktitle: FieldSeparatorChar
articleTitle: FieldSeparatorChar
second_title: Aspose.Words per .NET
description: Scopri come ControlChar FieldSeparatorChar migliora la gestione dei dati separando in modo efficace i codici di campo dai valori, ottimizzando il flusso di lavoro senza sforzi.
type: docs
weight: 90
url: /it/net/aspose.words/controlchar/fieldseparatorchar/
---
## ControlChar.FieldSeparatorChar field

Il carattere separatore di campo separa il codice di campo dal valore del campo. Facoltativo in alcuni campi. Valore: (char)20.

```csharp
public const char FieldSeparatorChar;
```

## Esempi

Mostra come aggiungere vari caratteri di controllo a un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiungi uno spazio normale.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Aggiungere un NBSP, che è uno spazio unificatore.
// A differenza dello spazio normale, questo spazio non può avere un'interruzione di riga automatica nella sua posizione.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Aggiunge un carattere di tabulazione.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Aggiungi un'interruzione di riga.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Aggiunge una nuova riga e inizia un nuovo paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Il carattere di avanzamento riga ha due versioni.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// I ritorni a capo e gli avanzamenti di riga possono essere rappresentati insieme da un carattere.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Aggiunge un'interruzione di paragrafo, che darà inizio a un nuovo paragrafo.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Aggiungi un'interruzione di sezione. Questo non crea una nuova sezione o un nuovo paragrafo.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Aggiungi un'interruzione di pagina.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Un'interruzione di pagina ha lo stesso valore di un'interruzione di sezione.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Inserisce una nuova sezione e imposta il numero di colonne su due.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Possiamo usare un carattere di controllo per contrassegnare il punto in cui il testo si sposta nella colonna successiva.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Per la maggior parte dei caratteri esistono le controparti char e string.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Guarda anche

* class [ControlChar](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
