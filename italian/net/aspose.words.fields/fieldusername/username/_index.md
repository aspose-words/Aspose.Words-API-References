---
title: FieldUserName.UserName
linktitle: UserName
articleTitle: UserName
second_title: Aspose.Words per .NET
description: Gestisci il nome dell'utente corrente senza problemi con la proprietà FieldUserName. Migliora l'esperienza utente e personalizza le interazioni in modo fluido.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gestisce o imposta il nome dell'utente corrente.

```csharp
public string UserName { get; set; }
```

## Esempi

Mostra come utilizzare il campo NOME UTENTE.

```csharp
Document doc = new Document();

// Creiamo un oggetto UserInformation e lo impostiamo come origine delle informazioni utente per tutti i campi che creiamo.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo USERNAME per visualizzare il nome dell'utente corrente,
// tratto dall'oggetto UserInformation creato sopra.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Ciò non influisce sul valore nell'oggetto UserInformation.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Guarda anche

* class [FieldUserName](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
