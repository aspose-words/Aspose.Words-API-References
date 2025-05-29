---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PreserveFormFields di PdfSaveOptions conserva i campi modulo di Microsoft Word nei PDF o li converte in testo. Migliora la qualità dei tuoi documenti!
type: docs
weight: 280
url: /it/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Specifica se conservare i campi del modulo di Microsoft Word come campi del modulo in PDF o convertirli in testo. Il valore predefinito è`falso` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Osservazioni

I campi del modulo di Microsoft Word includono controlli di immissione testo, menu a discesa e caselle di controllo.

Quando impostato su`falso` , questi campi verranno esportati come testo in PDF. Se impostato su`VERO`, questi campi verranno esportati come campi modulo PDF.

Quando si esportano i campi modulo in PDF come campi modulo, potrebbe verificarsi una perdita di formattazione perché i campi PDF form non supportano tutte le funzionalità dei campi modulo di Microsoft Word.

Inoltre, la dimensione dell'output dipende dalla dimensione del contenuto, poiché i moduli modificabili in Microsoft Word sono oggetti in linea.

I moduli modificabili sono vietati dalla conformità PDF/A.`falso` il valore verrà utilizzato automaticamente quando si salva in PDF/A.

I campi modulo non sono supportati durante il salvataggio in formato PDF/UA.`falso` il valore verrà utilizzato automaticamente.

## Esempi

Mostra come salvare un documento nel formato PDF utilizzando il metodo Save e la classe PdfSaveOptions.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Inserisce una casella combinata che consentirà all'utente di scegliere un'opzione da una raccolta di stringhe.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Impostare la proprietà "PreserveFormFields" su "true" per salvare i campi del modulo come oggetti interattivi nel PDF di output.
// Imposta la proprietà "PreserveFormFields" su "false" per bloccare tutti i campi del modulo nel documento
// i loro valori correnti e visualizzarli come testo normale nel PDF di output.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
