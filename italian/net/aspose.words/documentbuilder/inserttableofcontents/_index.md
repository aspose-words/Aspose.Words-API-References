---
title: DocumentBuilder.InsertTableOfContents
linktitle: InsertTableOfContents
articleTitle: InsertTableOfContents
second_title: Aspose.Words per .NET
description: Migliora senza sforzo i tuoi documenti con il metodo InsertTableOfContents di DocumentBuilder, aggiungendo un indice dinamico per una navigazione più semplice e una migliore organizzazione.
type: docs
weight: 500
url: /it/net/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder.InsertTableOfContents method

Inserisce un campo TOC (indice) nel documento.

```csharp
public Field InsertTableOfContents(string switches)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| switches | String | Il campo TOC cambia. |

## Osservazioni

Questo metodo inserisce un campo TOC (indice) nel documento nella posizione corrente.

Un indice in un documento Word può essere creato in diversi modi e formattato utilizzando diverse opzioni. Il modo in cui la tabella viene creata e visualizzata da Microsoft Word è controllato dai parametri di campo.

Il modo più semplice per specificare le opzioni è inserire e configurare un indice in un documento Word utilizzando il menu Inserisci-&gt;Riferimento-&gt;Indice e tabelle, quindi attivare la visualizzazione dei codici di campo per visualizzarle. È possibile premere Alt+F9 in Microsoft Word per attivare o disattivare la visualizzazione dei codici di campo.

Ad esempio, dopo aver creato un indice, il seguente campo viene inserito nel documento:**{ TOC \o "1-3" \h \z \u }** . Puoi copiare**\o "1-3" \h \z \u** e utilizzarlo come parametro switches.

Notare che`InsertTableOfContents` Inserirà solo un campo TOC, ma non creerà effettivamente il sommario. Il sommario viene creato da Microsoft Word quando il campo viene aggiornato.

Se si inserisce un indice utilizzando questo metodo e poi si apre il file in Microsoft Word, non verrà visualizzato l'indice perché il campo TOC non è ancora stato aggiornato.

In Microsoft Word, i campi non vengono aggiornati automaticamente quando si apre un documento, ma è possibile aggiornare i campi di un documento in qualsiasi momento premendo F9.

## Esempi

Mostra come inserire un indice (TOC) in un documento utilizzando gli stili di intestazione come voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un indice per la prima pagina del documento.
// Configura la tabella in modo che selezioni i paragrafi con titoli di livello da 1 a 3.
// Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il pulsante sinistro del mouse in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Popola il sommario aggiungendo paragrafi con stili di intestazione.
// Ciascuna intestazione con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
