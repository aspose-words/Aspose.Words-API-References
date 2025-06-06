---
title: UserInformation Class
linktitle: UserInformation
articleTitle: UserInformation
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fields.UserInformation pour gérer efficacement les détails des utilisateurs et améliorer le traitement des documents dans vos applications.
type: docs
weight: 3200
url: /fr/net/aspose.words.fields/userinformation/
---
## UserInformation class

Spécifie des informations sur l'utilisateur.

Pour en savoir plus, visitez le[Travailler avec les champs](https://docs.aspose.com/words/net/working-with-fields/) article de documentation.

```csharp
public class UserInformation
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [UserInformation](userinformation/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| static [DefaultUser](../../aspose.words.fields/userinformation/defaultuser/) { get; } | Informations utilisateur par défaut. |
| [Address](../../aspose.words.fields/userinformation/address/) { get; set; } | Obtient ou définit l'adresse postale de l'utilisateur. |
| [Initials](../../aspose.words.fields/userinformation/initials/) { get; set; } | Obtient ou définit les initiales de l'utilisateur. |
| [Name](../../aspose.words.fields/userinformation/name/) { get; set; } | Obtient ou définit le nom de l'utilisateur. |

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

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
