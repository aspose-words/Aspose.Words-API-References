---
title: Enum ParagraphAlignment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ParagraphAlignment enum. Specifica lallineamento del testo in un paragrafo.
type: docs
weight: 4160
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
| ArabicMediumKashida | `5` | solo arabo. La lunghezza di Kashida per il testo viene estesa a una lunghezza media determinata dal consumatore. |
| ArabicHighKashida | `7` | solo arabo. La lunghezza di Kashida per il testo viene estesa alla sua lunghezza più ampia possibile. |
| ArabicLowKashida | `8` | solo arabo. La lunghezza di Kashida per il testo è stata estesa a una lunghezza leggermente maggiore. |
| ThaiDistributed | `9` | solo tailandese. Il testo è giustificato con un'ottimizzazione per il tailandese. |
| MathElementCenterAsGroup | `10` | L'unico elemento Math in una riga, allineato come 'Centrato come gruppo'. |

### Esempi

Mostra come costruire manualmente un documento Aspose.Words.

```csharp
Document doc = new Document();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e finisci con un nodo documento senza figli.
doc.RemoveAllChildren();

// Questo documento ora non ha nodi figlio compositi a cui possiamo aggiungere contenuto.
// Se desideriamo modificarlo, dovremo ripopolare la sua raccolta di nodi.
// Innanzitutto, crea una nuova sezione, quindi aggiungila come figlio al nodo del documento radice.
Section section = new Section(doc);
doc.AppendChild(section);

// Imposta alcune proprietà di impostazione della pagina per la sezione.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutto il suo contenuto
// nella pagina tra l'intestazione e il piè di pagina della sezione.
Body body = new Body(doc);
section.AppendChild(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// Infine, aggiungi del contenuto per fare il documento. Crea una corsa,
// imposta l'aspetto e il contenuto, quindi aggiungilo come figlio al paragrafo.
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


