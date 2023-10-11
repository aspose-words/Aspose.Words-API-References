---
title: BuiltInDocumentProperties.Version
second_title: Aspose.Words per .NET API Reference
description: BuiltInDocumentProperties proprietà. Rappresenta il numero di versione dellapplicazione che ha creato il documento.
type: docs
weight: 320
url: /it/net/aspose.words.properties/builtindocumentproperties/version/
---
## BuiltInDocumentProperties.Version property

Rappresenta il numero di versione dell'applicazione che ha creato il documento.

```csharp
public int Version { get; set; }
```

### Osservazioni

Quando un documento è stato creato da Microsoft Word, i 16 bit alti rappresentano la versione principale e i 16 bit bassi rappresentano il numero di build.

### Esempi

Mostra come lavorare con le proprietà del documento nella categoria "Origine".

```csharp
// Apre un documento che abbiamo creato e modificato utilizzando Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Le seguenti proprietà integrate contengono informazioni relative alla creazione e alla modifica di questo documento.
// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare
// queste proprietà tramite "Proprietà" -> "Dettagli" -> Categoria "Origine".
// Campi come PRINTDATE e EDITTIME possono visualizzare questi valori nel corpo del documento.
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
// Per utilizzare queste proprietà con Aspose.Words, dovremo impostarne i valori manualmente.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Possiamo fare clic con il pulsante destro del mouse su questo documento in Esplora risorse e trovare these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../builtindocumentproperties/)
* assemblea [Aspose.Words](../../../)


