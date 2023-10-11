---
title: Enum ContentDisposition
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ContentDisposition enum. Enumera diversi modi di presentare il documento nel browser client.
type: docs
weight: 340
url: /it/net/aspose.words/contentdisposition/
---
## ContentDisposition enumeration

Enumera diversi modi di presentare il documento nel browser client.

```csharp
public enum ContentDisposition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Attachment | `0` | Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo nell'applicazione associata all'estensione del documento. |
| Inline | `1` | Invia il documento al browser e presenta un'opzione per salvare il documento su disco o aprirlo all'interno del browser. |

### Osservazioni

Tieni presente che il comportamento effettivo sul browser client potrebbe essere influenzato dalla configurazione di sicurezza del browser.

### Esempi

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
Assert.That(() => doc.Save(response, "Artifacts/MailMerge.ExecuteArray.docx", ContentDisposition.Inline, null),
    Throws.TypeOf<ArgumentNullException>()); //Generato perché HttpResponse è nullo nel test.

// Dovremo chiudere manualmente questa risposta per assicurarci di non aggiungere contenuti superflui al documento dopo il salvataggio.
Assert.That(() => response.End(), Throws.TypeOf<NullReferenceException>());
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


