---
title: ImportFormatMode Enum
linktitle: ImportFormatMode
articleTitle: ImportFormatMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words.ImportFormatMode migliora la formattazione dei documenti unendo perfettamente gli stili dei contenuti importati per risultati ottimali.
type: docs
weight: 3680
url: /it/net/aspose.words/importformatmode/
---
## ImportFormatMode enumeration

Specifica come viene unita la formattazione quando si importa contenuto da un altro documento.

```csharp
public enum ImportFormatMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| UseDestinationStyles | `0` | Utilizza gli stili del documento di destinazione e copia i nuovi stili. Questa è l'opzione predefinita. |
| KeepSourceFormatting | `1` | Copia tutti gli stili richiesti nel documento di destinazione, generando nomi di stile univoci se necessario. |
| KeepDifferentStyles | `2` | Copia solo gli stili diversi da quelli presenti nel documento di origine. |

## Osservazioni

Quando si copiano i nodi da un documento a un altro, questa opzione specifica come viene risolto formatting quando entrambi i documenti hanno uno stile con lo stesso nome, ma una formattazione diversa.

La formattazione viene risolta come segue:

1. Gli stili predefiniti vengono abbinati utilizzando il loro identificatore di stile indipendente dalle impostazioni locali. Gli stili definiti dall'utente vengono abbinati utilizzando un nome di stile con distinzione tra maiuscole e minuscole.
2. Se nel documento di destinazione non viene trovato uno stile corrispondente, lo stile (e tutti gli stili a cui fa riferimento) vengono copiati nel documento di destinazione e i nodi importati vengono aggiornati per fare riferimento al nuovo stile.
3. Se uno stile corrispondente esiste già nel documento di destinazione, ciò che accade dipende da`importFormatMode` parametro passato a [`ImportNode`](../documentbase/importnode/) come descritto di seguito.

Quando si utilizza ilUseDestinationStyles opzione, se uno stile corrispondente esiste già nel documento di destinazione, lo stile non viene copiato e i nodi importati vengono aggiornati per fare riferimento allo stile esistente.

Lo svantaggio dell'utilizzoUseDestinationStylesè che il testo importato potrebbe apparire diverso nel documento di destinazione rispetto al documento di origine. Ad esempio, lo stile "Titolo 1" nel documento di origine utilizza il carattere Arial 16pt e lo stile "Titolo 1" nel documento di destinazione utilizza il carattere Times New Roman 14pt. Quando si importa testo dello stile "Titolo 1" senza altra formattazione diretta, apparirà con il carattere Times New Roman 14pt nel documento di destinazione.

KeepSourceFormattingL'opzione consente di assicurarsi che il contenuto importato abbia lo stesso aspetto nel documento di destinazione rispetto al documento di origine. Se nel documento di destinazione esiste già uno stile corrispondente, la formattazione dello stile di origine viene espansa negli attributi diretti del nodo e lo stile viene modificato in Normale. Se lo stile non esiste nel documento di destinazione, lo stile di origine viene importato nel documento di destinazione e applicato al nodo importato. Si noti che non è sempre possibile preservare lo stile di origine anche se non esiste nel documento di destinazione. In questo caso la formattazione di tale stile verrà espansa negli attributi diretti del nodo a favore della conservazione della formattazione originale del nodo.

Lo svantaggio dell'utilizzoKeepSourceFormattingè che se si eseguono più importazioni, si potrebbero ritrovare molti stili nel documento di destinazione e ciò potrebbe rendere difficoltoso l'utilizzo di una formattazione di stile coerente in Microsoft Word per questo documento.

UtilizzoKeepDifferentStyles L'opzione consente di riutilizzare gli stili di destinazione se la formattazione fornita è identica agli stili nel documento di origine. Se lo stile nel documento di destinazione è diverso da quello di origine, viene importato.

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
