---
title: FieldUserName.UserName
second_title: Aspose.Words per .NET API Reference
description: FieldUserName proprietà. Gestisci o imposta il nome dellutente corrente.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gestisci o imposta il nome dell'utente corrente.

```csharp
public string UserName { get; set; }
```

### Esempi

Mostra come utilizzare il campo USERNAME.

```csharp
Document doc = new Document();

// Crea un oggetto UserInformation e impostalo come origine delle informazioni sull'utente per tutti i campi che creiamo.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo USERNAME per visualizzare il nome dell'utente corrente,
// tratto dall'oggetto UserInformation che abbiamo creato sopra.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Possiamo impostare questa proprietà per fare in modo che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
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
* spazio dei nomi [Aspose.Words.Fields](../../fieldusername/)
* assemblea [Aspose.Words](../../../)


