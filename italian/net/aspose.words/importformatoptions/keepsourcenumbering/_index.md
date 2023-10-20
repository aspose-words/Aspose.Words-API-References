---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words per .NET
description: ImportFormatOptions KeepSourceNumbering proprietà. Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione in caso di conflitto nei documenti di origine e di destinazione. Il valore predefinito èfalso  in C#.
type: docs
weight: 60
url: /it/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione in caso di conflitto nei documenti di origine e di destinazione. Il valore predefinito è`falso` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Esempi

Mostra come risolvere un'interferenza durante l'importazione di documenti che presentano elenchi con lo stesso identificatore di definizione di elenco.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Imposta la proprietà "KeepSourceNumbering" su "true" per applicare un ID di definizione elenco diverso
// a stili identici poiché Aspose.Words li importa nei documenti di destinazione.
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

// Se c'è un conflitto di stili di elenco, applica il formato elenco del documento di origine.
// Imposta la proprietà "KeepSourceNumbering" su "false" per non importare alcun numero di elenco nel documento di destinazione.
// Imposta la proprietà "KeepSourceNumbering" su "true" per importare tutti i conflitti
// numerazione dello stile dell'elenco con lo stesso aspetto che aveva nel documento di origine.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Mostra come risolvere i conflitti di numerazione degli elenchi nei documenti di origine e di destinazione.

```csharp
// Apre un documento con uno schema di numerazione dell'elenco personalizzato, quindi clonalo.
// Poiché entrambi hanno lo stesso formato di numerazione, i formati entreranno in conflitto se importiamo un documento nell'altro.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Quando importiamo il clone del documento nell'originale e poi lo aggiungiamo,
// quindi i due elenchi con lo stesso formato di elenco verranno uniti.
// Se impostiamo il flag "KeepSourceNumbering" su "false", l'elenco dal clone del documento
// che aggiungiamo all'originale porterà avanti la numerazione dell'elenco a cui lo aggiungiamo.
// Ciò unirà effettivamente i due elenchi in uno solo.
// Se impostiamo il flag "KeepSourceNumbering" su "true", il documento verrà clone
 // la lista manterrà la sua numerazione originale, facendo apparire le due liste come liste separate.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
