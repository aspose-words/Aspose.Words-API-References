---
title: Document.RemovePersonalInformation
linktitle: RemovePersonalInformation
articleTitle: RemovePersonalInformation
second_title: Aspose.Words per .NET
description: Garantisci la privacy con la funzionalità Rimuovi informazioni personali dal documento in Word, eliminando automaticamente i dati utente dai commenti e dalle proprietà al momento del salvataggio.
type: docs
weight: 360
url: /it/net/aspose.words/document/removepersonalinformation/
---
## Document.RemovePersonalInformation property

Ottiene o imposta un flag che indica che Microsoft Word rimuoverà tutte le informazioni utente dai commenti, dalle revisioni e dalle proprietà del documento al momento del salvataggio del documento.

```csharp
public bool RemovePersonalInformation { get; set; }
```

## Esempi

Mostra come abilitare la rimozione delle informazioni personali durante un salvataggio manuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire del contenuto con informazioni personali.
doc.BuiltInDocumentProperties.Author = "John Doe";
doc.BuiltInDocumentProperties.Company = "Placeholder Inc.";

doc.StartTrackRevisions(doc.BuiltInDocumentProperties.Author, DateTime.Now);
builder.Write("Hello world!");
doc.StopTrackRevisions();

// Questo flag è equivalente a File -> Opzioni -> Centro protezione -> Impostazioni Centro protezione... ->
// Opzioni privacy -> "Rimuovi informazioni personali dalle proprietà del file al salvataggio" in Microsoft Word.
doc.RemovePersonalInformation = saveWithoutPersonalInfo;

// Questa opzione non avrà effetto durante un'operazione di salvataggio effettuata tramite Aspose.Words.
// I dati personali verranno rimossi dal nostro documento con il flag impostato quando lo salviamo manualmente utilizzando Microsoft Word.
doc.Save(ArtifactsDir + "Document.RemovePersonalInformation.docx");
doc = new Document(ArtifactsDir + "Document.RemovePersonalInformation.docx");

Assert.AreEqual(saveWithoutPersonalInfo, doc.RemovePersonalInformation);
Assert.AreEqual("John Doe", doc.BuiltInDocumentProperties.Author);
Assert.AreEqual("Placeholder Inc.", doc.BuiltInDocumentProperties.Company);
Assert.AreEqual("John Doe", doc.Revisions[0].Author);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
