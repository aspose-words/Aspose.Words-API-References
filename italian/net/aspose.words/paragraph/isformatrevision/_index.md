---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words per .NET
description: Paragraph IsFormatRevision proprietà. Restituisce true se la formattazione delloggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche in C#.
type: docs
weight: 90
url: /it/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre era abilitato il rilevamento delle modifiche.

```csharp
public bool IsFormatRevision { get; }
```

## Esempi

Mostra come verificare se un paragrafo è una revisione del formato.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Questo paragrafo è una revisione del "Formato", che si verifica quando modifichiamo la formattazione del testo esistente
// durante il monitoraggio delle revisioni in Microsoft Word tramite "Revisione" -> "Tenere traccia delle modifiche".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
