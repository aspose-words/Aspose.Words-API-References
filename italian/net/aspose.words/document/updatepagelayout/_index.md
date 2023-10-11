---
title: Document.UpdatePageLayout
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Ricostruisce limpaginazione del documento.
type: docs
weight: 790
url: /it/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

Ricostruisce l'impaginazione del documento.

```csharp
public void UpdatePageLayout()
```

### Osservazioni

Questo metodo formatta un documento in pagine e aggiorna i campi relativi al numero di pagina nel documento come come PAGE, PAGES, PAGEREF e REF. Le informazioni aggiornate sul layout della pagina sono necessarie per un corretto rendering del documento nei formati a pagina fissa.

Questo metodo viene richiamato automaticamente quando si converte per la prima volta un documento in PDF, XPS, immagine o lo si stampa. Tuttavia, se si modifica il documento dopo il rendering e quindi si tenta di eseguirne nuovamente il rendering, Aspose.Words non aggiornerà automaticamente il layout della pagina. In questo caso dovresti chiamare`UpdatePageLayout` prima rendering di nuovo.

### Esempi

Mostra quando ricalcolare il layout di pagina del documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Il salvataggio di un documento in PDF, in un'immagine o la stampa per la prima volta avverrà automaticamente
// memorizza nella cache il layout del documento all'interno delle sue pagine.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Modifica il documento in qualche modo.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // Nella versione corrente di Aspose.Words, la modifica del documento non viene ricostruita automaticamente
// il layout della pagina memorizzata nella cache. Se desideriamo il layout memorizzato nella cache
// per rimanere aggiornati, dovremo aggiornarlo manualmente.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


