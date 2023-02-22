---
title: ImportFormatOptions.KeepSourceNumbering
second_title: Aspose.Words per .NET API Reference
description: ImportFormatOptions proprietà. Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando si verifica un conflitto nei documenti di origine e di destinazione. Il valore predefinito èfalso .
type: docs
weight: 50
url: /it/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando si verifica un conflitto nei documenti di origine e di destinazione. Il valore predefinito è`falso` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

### Esempi

Mostra come risolvere un conflitto durante l'importazione di documenti che hanno elenchi con lo stesso identificatore di definizione elenco.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Imposta la proprietà "KeepSourceNumbering" su "true" per applicare un ID di definizione elenco diverso
// in stili identici a quelli di Aspose.Words li importa nei documenti di destinazione.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Mostra come importare un documento con elenchi numerati.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// In caso di conflitto di stili di elenco, applica il formato elenco del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di elenco nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" importa tutte le interferenze
// numerazione degli stili di elenco con lo stesso aspetto che aveva nel documento di origine.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e di destinazione.

```csharp
// Apre un documento con uno schema di numerazione elenco personalizzato, quindi clonalo.
// Poiché entrambi hanno lo stesso formato di numerazione, i formati si scontreranno se importiamo un documento nell'altro.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Quando importiamo il clone del documento nell'originale e poi lo aggiungiamo,
// quindi si uniranno i due elenchi con lo stesso formato di elenco.
// Se impostiamo il flag "KeepSourceNumbering" su "false", l'elenco dal documento clone
// che aggiungiamo all'originale continuerà la numerazione dell'elenco a cui lo aggiungiamo.
// Questo unirà efficacemente le due liste in una sola.
// Se impostiamo il flag "KeepSourceNumbering" su "true", il documento clona
// list manterrà la sua numerazione originale, facendo apparire le due liste come liste separate. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../importformatoptions/)
* assemblea [Aspose.Words](../../../)


