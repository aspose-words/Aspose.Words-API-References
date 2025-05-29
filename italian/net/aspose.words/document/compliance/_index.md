---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words per .NET
description: Assicura che i tuoi documenti OOXML soddisfino senza problemi gli standard di conformità. Il nostro strumento analizza i contenuti per verificarne la conformità OOXML, migliorando l'integrità dei documenti.
type: docs
weight: 70
url: /it/net/aspose.words/document/compliance/
---
## Document.Compliance property

Ottiene la versione di conformità OOXML determinata dal contenuto del documento caricato. Ha senso solo per i documenti OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Osservazioni

Se hai creato un nuovo documento vuoto o hai caricato un documento non OOXML, il documento restituisceEcma376_2006 valore.

## Esempi

Mostra come leggere la versione conforme a Open Office XML di un documento caricato.

```csharp
// La versione di conformità varia tra i documenti creati con diverse versioni di Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Guarda anche

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
