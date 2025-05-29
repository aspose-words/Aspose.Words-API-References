---
title: UserInformation.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words pour .NET
description: Gérez facilement les profils utilisateur grâce à la propriété UserInformation Name. Récupérez ou mettez à jour facilement les noms d'utilisateur pour une personnalisation optimisée.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/userinformation/name/
---
## UserInformation.Name property

Obtient ou définit le nom de l'utilisateur.

```csharp
public string Name { get; set; }
```

## Exemples

Montre comment définir les détails de l'utilisateur et les afficher à l'aide de champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créez un objet UserInformation et définissez-le comme source de données pour les champs qui affichent des informations utilisateur.
UserInformation userInformation = new UserInformation
{
    Name = "John Doe",
    Initials = "J. D.",
    Address = "123 Main Street"
};
doc.FieldOptions.CurrentUser = userInformation;

// Insérer les champs USERNAME, USERINITIALS et USEADDRESS, qui affichent les valeurs de
 // les propriétés respectives de l'objet UserInformation que nous avons créé ci-dessus.
Assert.AreEqual(userInformation.Name, builder.InsertField(" USERNAME ").Result);
Assert.AreEqual(userInformation.Initials, builder.InsertField(" USERINITIALS ").Result);
Assert.AreEqual(userInformation.Address, builder.InsertField(" USERADDRESS ").Result);

// L'objet d'options de champ dispose également d'un utilisateur par défaut statique auquel les champs de tous les documents peuvent faire référence.
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

### Voir également

* class [UserInformation](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
