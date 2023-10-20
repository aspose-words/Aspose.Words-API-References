---
title: ControlChar.FieldStartChar
linktitle: FieldStartChar
articleTitle: FieldStartChar
second_title: Aspose.Words per .NET
description: ControlChar FieldStartChar campo. Carattere iniziale del campo MS Word char19 in C#.
type: docs
weight: 100
url: /it/net/aspose.words/controlchar/fieldstartchar/
---
## ControlChar.FieldStartChar field

Carattere iniziale del campo MS Word: (char)19.

```csharp
public const char FieldStartChar;
```

## Esempi

Mostra come aggiungere vari caratteri di controllo a un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunge uno spazio regolare.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Aggiunge un NBSP, che è uno spazio unificatore.
// A differenza dello spazio normale, questo spazio non può avere un'interruzione di riga automatica nella sua posizione.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Aggiunge un carattere di tabulazione.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Aggiunge un'interruzione di riga.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Aggiunge una nuova riga e inizia un nuovo paragrafo.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Il carattere di avanzamento riga ha due versioni.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// I ritorni a capo e gli avanzamenti di riga possono essere rappresentati insieme da un carattere.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Aggiunge un'interruzione di paragrafo, che inizierà un nuovo paragrafo.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Aggiunge un'interruzione di sezione. Ciò non crea una nuova sezione o paragrafo.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Aggiunge un'interruzione di pagina.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Un'interruzione di pagina ha lo stesso valore di un'interruzione di sezione.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Inserisci una nuova sezione, quindi imposta il numero di colonne su due.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Possiamo usare un carattere di controllo per contrassegnare il punto in cui il testo si sposta alla colonna successiva.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Esistono controparti char e string per la maggior parte dei caratteri.
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
