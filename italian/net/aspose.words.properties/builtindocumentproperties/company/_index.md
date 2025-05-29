---
title: BuiltInDocumentProperties.Company
linktitle: Company
articleTitle: Company
second_title: Aspose.Words per .NET
description: Gestisci le tue BuiltInDocumentProperties senza sforzo. Ottieni o imposta facilmente le proprietà aziendali per migliorare l'organizzazione dei documenti e semplificare i flussi di lavoro.
type: docs
weight: 70
url: /it/net/aspose.words.properties/builtindocumentproperties/company/
---
## BuiltInDocumentProperties.Company property

Ottiene o imposta la proprietà aziendale.

```csharp
public string Company { get; set; }
```

## Esempi

Mostra come lavorare con le proprietà del documento nella categoria "Origine".

```csharp
// Apriamo un documento che abbiamo creato e modificato utilizzando Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Le seguenti proprietà integrate contengono informazioni relative alla creazione e alla modifica di questo documento.
// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare
// queste proprietà tramite la categoria "Proprietà" -> "Dettagli" -> "Origine".
// Campi come PRINTDATE ed EDITTIME possono visualizzare questi valori nel corpo del documento.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Possiamo anche modificare i valori delle proprietà integrate.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word aggiorna automaticamente le seguenti proprietà quando salviamo il documento.
// Per utilizzare queste proprietà con Aspose.Words, dovremo impostare manualmente i relativi valori.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
