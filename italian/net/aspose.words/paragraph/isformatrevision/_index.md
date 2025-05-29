---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IsFormatRevision in Microsoft Word tiene traccia delle modifiche di formattazione, garantendo modifiche accurate ai documenti e una migliore collaborazione.
type: docs
weight: 90
url: /it/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il rilevamento delle modifiche era abilitato.

```csharp
public bool IsFormatRevision { get; }
```

## Esempi

Mostra come verificare se un paragrafo è una revisione del formato.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Questo paragrafo è una revisione del "Formato", che si verifica quando modifichiamo la formattazione del testo esistente
// durante il monitoraggio delle revisioni in Microsoft Word tramite "Revisione" -> "Traccia modifiche".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
