---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words per .NET
description: Aspose.Words.ImportFormatMode enum. Specifica la modalità di unione della formattazione durante limportazione di contenuto da un altro documento in C#.
type: docs
weight: 3230
url: /it/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Specifica la modalità di unione della formattazione durante l'importazione di contenuto da un altro documento.

```csharp
public enum ImportFormatMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseDestinationStyles | `0` | Utilizza gli stili del documento di destinazione e copia nuovi stili. Questa è l'opzione predefinita. |
| KeepSourceFormatting | `1` | Copia tutti gli stili richiesti nel documento di destinazione, genera nomi di stile univoci se necessario. |
| KeepDifferentStyles | `2` | Copia solo gli stili diversi da quelli del documento di origine. |

## Osservazioni

Quando copi i nodi da un documento a un altro, questa opzione specifica come viene risolto formatting quando entrambi i documenti hanno uno stile con lo stesso nome, ma formattazione diversa.

La formattazione viene risolta come segue:

1. Gli stili incorporati vengono abbinati utilizzando il relativo identificatore di stile indipendente dalle impostazioni locali. Gli stili definiti dall'utente vengono abbinati utilizzando il nome di stile con distinzione tra maiuscole e minuscole.
2. Se uno stile corrispondente non viene trovato nel documento di destinazione, style (e tutti gli stili a cui fa riferimento) vengono copiati nel documento di destinazione document e i nodi importati vengono aggiornati per fare riferimento al nuovo stile.
3. Se uno stile corrispondente esiste già nel documento di destinazione, ciò che accade dipende da`importFormatMode` parametro passato a [`Document.ImportNode`](../documentbase/importnode/) come descritto di seguito.

Quando si utilizza ilUseDestinationStyles opzione, se uno stile corrispondente esiste già nel documento di destinazione, lo stile non viene copiato e i nodi importati vengono aggiornati per fare riferimento allo stile esistente.

Lo svantaggio dell'utilizzoUseDestinationStylesè che il testo importato potrebbe apparire diverso nel documento di destinazione rispetto al documento di origine. Ad esempio, lo stile "Intestazione 1" nel documento di origine utilizza il carattere Arial 16pt e lo stile "Intestazione 1" nel documento di destinazione utilizza Times New Carattere Roman 14pt. Quando si importa testo con stile "Intestazione 1" senza altra formattazione diretta, verrà visualizzato come carattere Times New Roman 14pt nel documento di destinazione.

KeepSourceFormattingl'opzione consente di assicurarsi che il contenuto importato abbia lo stesso nel documento di destinazione così come appare nel documento di origine. Se uno stile corrispondente esiste già nel documento di destinazione, la formattazione dello stile di origine viene espansa negli attributi diretti del Nodo e lo stile è cambiato in Normale. Se lo stile non esiste nel documento di destinazione, lo stile di origine viene importato nel documento di destinazione e applicato al nodo importato. Nota che non è sempre possibile preservare lo stile di origine anche se non esiste nel documento di destinazione. In questo caso la formattazione di tale stile verrà espansa negli attributi diretti del Nodo a favore della conservazione della formattazione originale del Nodo.

Lo svantaggio dell'utilizzoKeepSourceFormattingè che se esegui diverse importazioni, potresti ritrovarti con molti stili nel documento di destinazione e ciò potrebbe rendere difficile l'utilizzo di formattazione di stili coerenti in Microsoft Word per questo documento.

UtilizzandoKeepDifferentStyles l'opzione consente di riutilizzare gli stili di destinazione se la formattazione fornita è identica agli stili nel documento di origine. Se lo stile nel documento di destinazione è diverso dall'origine, viene importato.

## Esempi

Mostra come inserire un documento in un altro documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
