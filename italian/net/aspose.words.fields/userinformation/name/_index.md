---
title: UserInformation.Name
second_title: Aspose.Words per .NET API Reference
description: UserInformation proprietà. Ottiene o imposta il nome dellutente.
type: docs
weight: 50
url: /it/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

Ottiene o imposta il nome dell'utente.

```csharp
public string Name { get; set; }
```

### Esempi

Mostra come impostare i dettagli utente e visualizzarli utilizzando i campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni sull'utente.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Inserisce i campi USERNAME, USERINITIALS e USERADDRESS, che mostrano i valori di
// le rispettive proprietà dell'oggetto UserInformation che abbiamo creato sopra. 
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// L'oggetto opzioni campo ha anche un utente predefinito statico a cui possono fare riferimento i campi di tutti i documenti.
UserInformation.DefaultUser.Name = "Default User";
UserInformation.DefaultUser.Initials = "D. U.";
UserInformation.DefaultUser.Address = "One Microsoft Way";
doc.FieldOptions.CurrentUser = UserInformation.DefaultUser;

Assert.AreEqual("Default User", builder.InsertField(" USERNAME ").Result);
Assert.AreEqual("D. U.", builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual("One Microsoft Way", builder.InsertField(" USERADDRESS ").Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.CurrentUser.docx");
```

### Guarda anche

* class [UserInformation](../)
* spazio dei nomi [Aspose.Words.Fields](../../userinformation/)
* assemblea [Aspose.Words](../../../)


