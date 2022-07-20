---
title: UserAddress
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta lindirizzo postale dellutente corrente.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Ottiene o imposta l'indirizzo postale dell'utente corrente.

```csharp
public string UserAddress { get; set; }
```

### Esempi

Mostra come utilizzare il campo USERADDRESS.

```csharp
Document doc = new Document();

// Crea un oggetto UserInformation e impostalo come fonte di informazioni sull'utente per tutti i campi che creiamo.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Crea un campo USERADDRESS per visualizzare l'indirizzo dell'utente corrente,
// preso dall'oggetto UserInformation che abbiamo creato sopra.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

 // Possiamo impostare questa proprietà per fare in modo che il nostro campo sostituisca il valore attualmente memorizzato nell'oggetto UserInformation.
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

* class [FieldUserAddress](../../fielduseraddress)
* spazio dei nomi [Aspose.Words.Fields](../../fielduseraddress)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->