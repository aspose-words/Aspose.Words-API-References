---
title: UserInformation.Initials
linktitle: Initials
articleTitle: Initials
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà UserInformation Initials per gestire e personalizzare facilmente le iniziali degli utenti, per una personalizzazione e un'esperienza utente ottimizzate.
type: docs
weight: 40
url: /it/net/aspose.words.fields/userinformation/initials/
---
## UserInformation.Initials property

Ottiene o imposta le iniziali dell'utente.

```csharp
public string Initials { get; set; }
```

## Esempi

Mostra come impostare i dettagli dell'utente e visualizzarli utilizzando i campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un oggetto UserInformation e impostalo come origine dati per i campi che visualizzano le informazioni utente.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Inserire i campi USERNAME, USERINITIALS e USERADDRESS, che visualizzano i valori di
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
