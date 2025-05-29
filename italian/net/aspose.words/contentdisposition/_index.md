---
title: ContentDisposition Enum
linktitle: ContentDisposition
articleTitle: ContentDisposition
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.ContentDisposition per scoprire diverse opzioni di presentazione dei documenti per migliorare l'esperienza del browser client.
type: docs
weight: 540
url: /it/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Enumera i diversi modi di presentare il documento nel browser client.

```csharp
public enum ContentDisposition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Attachment | `0` | Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo nell'applicazione associata all'estensione del documento. |
| Inline | `1` | Invia il documento al browser e presenta un'opzione per salvare il documento sul disco o aprirlo all'interno del browser. |

## Osservazioni

Si noti che il comportamento effettivo del browser client potrebbe essere influenzato dalla configurazione di sicurezza del browser.

## Esempi

Mostra come eseguire una stampa unione e quindi salvare il documento nel browser client.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FullName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Company ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD Address ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

doc.MailMerge.Execute(new string[] { "FullName", "Company", "Address", "City" },
    new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Invia il documento al browser client.
//Generato perché HttpResponse è null nel test.
Assert.Throws<ArgumentNullException>(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null));

// Dovremo chiudere manualmente questa risposta per assicurarci di non aggiungere contenuti superflui al documento dopo il salvataggio.
Assert.Throws<NullReferenceException>(() => response.End());
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
