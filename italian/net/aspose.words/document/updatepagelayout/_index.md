---
title: Document.UpdatePageLayout
linktitle: UpdatePageLayout
articleTitle: UpdatePageLayout
second_title: Aspose.Words per .NET
description: Rinnova la struttura del tuo documento con il metodo UpdatePageLayout, assicurando un layout ordinato e rifinito per una migliore leggibilità e presentazione.
type: docs
weight: 830
url: /it/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Ricostruisce il layout di pagina del documento.

```csharp
public void UpdatePageLayout()
```

## Osservazioni

Questo metodo formatta un documento in pagine e aggiorna i campi relativi al numero di pagina nel documento, come PAGE, PAGES, PAGEREF e REF. Le informazioni aggiornate sul layout di pagina sono necessarie per una corretta visualizzazione del documento in formati a pagina fissa.

Questo metodo viene richiamato automaticamente quando si converte per la prima volta un documento in PDF, XPS, immagine o lo si stampa. Tuttavia, se si modifica il documento dopo il rendering e poi si tenta di eseguirne un altro, Aspose.Words non aggiornerà automaticamente il layout di pagina. In questo caso, è necessario chiamare`UpdatePageLayout` prima di eseguire nuovamente il rendering.

## Esempi

Indica quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta verranno eseguiti automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modificare il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// Nella versione corrente di Aspose.Words, la modifica del documento non ne comporta la ricostruzione automatica
// il layout della pagina memorizzato nella cache. Se desideriamo il layout memorizzato nella cache
// Per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
