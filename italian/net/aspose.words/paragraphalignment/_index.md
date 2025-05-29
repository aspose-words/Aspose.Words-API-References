---
title: ParagraphAlignment Enum
linktitle: ParagraphAlignment
articleTitle: ParagraphAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.ParagraphAlignment per un allineamento preciso del testo nei tuoi documenti. Migliora la leggibilità e la formattazione con facilità!
type: docs
weight: 5130
url: /it/net/aspose.words/paragraphalignment/
---
## ParagraphAlignment enumeration

Specifica l'allineamento del testo in un paragrafo.

```csharp
public enum ParagraphAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Left | `0` | Il testo è allineato a sinistra. |
| Center | `1` | Il testo è centrato orizzontalmente. |
| Right | `2` | Il testo è allineato a destra. |
| Justify | `3` | Il testo è allineato sia a sinistra che a destra. |
| Distributed | `4` | Il testo è distribuito uniformemente. |
| ArabicMediumKashida | `5` | Solo in arabo. La lunghezza del testo in kashida è estesa a una lunghezza media, determinata dal consumatore. |
| ArabicHighKashida | `7` | Solo in arabo. La lunghezza del testo in kashida è estesa alla sua massima lunghezza possibile. |
| ArabicLowKashida | `8` | Solo in arabo. La lunghezza del testo in Kashida è leggermente maggiore. |
| ThaiDistributed | `9` | Solo in tailandese. Il testo è giustificato con un'ottimizzazione per il tailandese. |
| MathElementCenterAsGroup | `10` | L'unico elemento Math in una riga, allineato come 'Centrato come gruppo'. |

## Esempi

Mostra come creare manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e si finisce con un nodo documento senza elementi figlio.
doc.RemoveAllChildren();

// Questo documento non ha più nodi figlio compositi a cui aggiungere contenuto.
// Se volessimo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlia al nodo radice del documento.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e poi aggiungilo come elemento secondario al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per completare il documento. Crea una run,
// impostane l'aspetto e il contenuto, quindi aggiungilo come elemento figlio al paragrafo.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
