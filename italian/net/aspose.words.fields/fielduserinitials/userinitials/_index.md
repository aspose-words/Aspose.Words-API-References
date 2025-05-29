---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words per .NET
description: Accedi e personalizza la proprietà FieldUserInitials per gestire senza sforzo le iniziali degli utenti, migliorando la personalizzazione e l'esperienza utente.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Ottiene o imposta le iniziali dell'utente corrente.

```csharp
public string UserInitials { get; set; }
```

## Esempi

Mostra come utilizzare il campo USERINITIALS.

```csharp
Document doc = new Document();

// Creiamo un oggetto UserInformation e lo impostiamo come origine delle informazioni utente per tutti i campi che creiamo.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Crea un campo USERINITIALS per visualizzare le iniziali dell'utente corrente,
// tratto dall'oggetto UserInformation creato sopra.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Ciò non influisce sul valore nell'oggetto UserInformation.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Guarda anche

* class [FieldUserInitials](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
