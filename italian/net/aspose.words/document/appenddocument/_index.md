---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: Aspose.Words per .NET
description: Aggiungi documenti senza sforzo con il nostro metodo "Document Append". Migliora il tuo flusso di lavoro integrando perfettamente i contenuti nei file esistenti.
type: docs
weight: 570
url: /it/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

Aggiunge il documento specificato alla fine di questo documento.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Il documento da allegare. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione di stile in conflitto. |

## Esempi

Mostra come aggiungere un documento alla fine di un altro documento.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Aggiungi il documento sorgente al documento di destinazione preservandone la formattazione,
// quindi salva il documento sorgente nel file system locale.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Mostra come aggiungere tutti i documenti in una cartella alla fine di un documento modello.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// Aggiungi tutti i documenti non crittografati con estensione .doc
// dalla directory del nostro file system locale al documento base.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Guarda anche

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

Aggiunge il documento specificato alla fine di questo documento.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcDoc | Document | Il documento da allegare. |
| importFormatMode | ImportFormatMode | Specifica come unire la formattazione di stile in conflitto. |
| importFormatOptions | ImportFormatOptions | Consente di specificare le opzioni che influiscono sulla formattazione di un documento risultante. |

## Esempi

Mostra come gestire i conflitti di stile degli elenchi durante l'aggiunta di un clone di un documento a se stesso.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// In caso di conflitto di stili di elenco, applicare il formato di elenco del documento di origine.
// Impostare la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di elenco nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// elenca la numerazione in stile con lo stesso aspetto che aveva nel documento sorgente.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Mostra come gestire i conflitti di stile degli elenchi durante l'inserimento di un documento.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// In caso di conflitto di stili di elenco, applicare il formato di elenco del documento di origine.
// Impostare la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di elenco nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// elenca la numerazione in stile con lo stesso aspetto che aveva nel documento sorgente.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Mostra come gestire i conflitti di stile degli elenchi durante l'aggiunta di un documento.

```csharp
// Carica un documento con testo in uno stile personalizzato e clonalo.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Ora abbiamo due documenti, ciascuno con uno stile identico denominato "CustomStyle".
// Cambia il colore del testo di uno degli stili per distinguerlo dall'altro.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// In caso di conflitto di stili di elenco, applicare il formato di elenco del documento di origine.
// Impostare la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di elenco nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// elenca la numerazione in stile con lo stesso aspetto che aveva nel documento sorgente.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// L'unione di due documenti con stili diversi che condividono lo stesso nome provoca un conflitto di stili.
// Possiamo specificare una modalità di formato di importazione durante l'aggiunta di documenti per risolvere questo conflitto.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Guarda anche

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
