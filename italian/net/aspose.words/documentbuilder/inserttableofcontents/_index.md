---
title: DocumentBuilder.InsertTableOfContents
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Inserisce un campo TOC indice nel documento.
type: docs
weight: 440
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

### Osservazioni

Questo metodo inserisce un campo TOC (indice) nel documento in nella posizione corrente.

Un sommario in un documento di Word può essere creato in diversi modi e formattato utilizzando una varietà di opzioni. Il modo in cui la tabella è costruita e visualizzata da Microsoft Word è controllata dalle opzioni di campo.

Il modo più semplice per specificare le opzioni è inserire e configurare una tabella di contenuti in un documento di Word utilizzando il menu Inserisci-&gt;Riferimento-&gt;Indice e tabelle, quindi attivare la visualizzazione dei codici di campo per visualizzare le opzioni. È possibile premere Alt+F9 in Microsoft Word per attivare o disattivare la visualizzazione dei codici di campo.

Ad esempio, dopo aver creato un sommario, nel documento viene inserito il seguente campo : **{ TOC \o "1-3" \h \z \u }** . Puoi copiare **\o "1-3" \h \z \u** e usalo come parametro switch.

Notare che **InserisciTableOfContents** inserirà solo un campo TOC, ma non creerà effettivamente il sommario. Il sommario viene creato da Microsoft Word quando il campo viene aggiornato.

Se inserisci un sommario utilizzando questo metodo e poi apri il file in Microsoft Word, non vedrai il sommario perché il campo TOC non è stato ancora aggiornato.

In Microsoft Word, i campi non vengono aggiornati automaticamente all'apertura di un documento, , ma puoi aggiornare i campi di un documento in qualsiasi momento premendo F9.

### Esempi

Mostra come inserire un sommario (TOC) in un documento utilizzando gli stili di intestazione come voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un sommario per la prima pagina del documento.
// Configura la tabella per raccogliere paragrafi con intestazioni di livello da 1 a 3.
// Inoltre, imposta le sue voci in modo che siano collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il pulsante sinistro del mouse in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Popolare il sommario aggiungendo paragrafi con stili di intestazione.
// Ciascuna di queste intestazioni con un livello compreso tra 1 e 3 creerà una voce nella tabella.
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

// Un sommario è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Guarda anche

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


