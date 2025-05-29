---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words per .NET
description: Gestisci gli indirizzi postali degli utenti senza sforzo con la proprietà FieldUserAddress. Recupera e aggiorna facilmente le informazioni utente correnti per un'esperienza migliore.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Ottiene o imposta l'indirizzo postale dell'utente corrente.

```csharp
public string UserAddress { get; set; }
```

## Esempi

Mostra come utilizzare il campo USERADDRESS.

```csharp
Document doc = new Document();

// Creiamo un oggetto UserInformation e lo impostiamo come origine delle informazioni utente per tutti i campi che creiamo.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Crea un campo USERADDRESS per visualizzare l'indirizzo dell'utente corrente,
// tratto dall'oggetto UserInformation creato sopra.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// Possiamo impostare questa proprietà per far sì che il nostro campo sovrascriva il valore attualmente memorizzato nell'oggetto UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Ciò non influisce sul valore nell'oggetto UserInformation.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Guarda anche

* class [FieldUserAddress](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
