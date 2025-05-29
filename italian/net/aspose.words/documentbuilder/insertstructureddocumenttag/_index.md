---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti senza sforzo con il metodo InsertStructuredDocumentTag di DocumentBuilder. Aggiungi facilmente tag strutturati ai documenti per una migliore organizzazione!
type: docs
weight: 480
url: /it/net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Inserisce un[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) nel documento.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Valore di ritorno

IL[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) nodo appena inserito.

## Esempi

Mostra come inserire semplicemente il tag di un documento strutturato.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Nota che è consentito l'inserimento solo dei seguenti tipi StructuredDocumentTag:
// SdtType.Testo normale, SdtType.RichText, SdtType.Casella di controllo, SdtType.Elenco a discesa,
// SdtType.ComboBox, SdtType.Immagine, SdtType.Data.
// Il livello di markup dello StructuredDocumentTag inserito verrà rilevato automaticamente e dipenderà dalla posizione in cui viene inserito.
// Aggiunto StructuredDocumentTag erediterà la formattazione del paragrafo e del carattere dalla posizione del cursore.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### Guarda anche

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
