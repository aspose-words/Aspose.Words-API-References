---
title: FieldUserAddress.UserAddress
linktitle: UserAddress
articleTitle: UserAddress
second_title: Aspose.Words pour .NET
description: Gérez facilement les adresses postales des utilisateurs grâce à la propriété FieldUserAddress. Récupérez et mettez à jour facilement les informations des utilisateurs actuels pour une expérience optimisée.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fielduseraddress/useraddress/
---
## FieldUserAddress.UserAddress property

Obtient ou définit l'adresse postale de l'utilisateur actuel.

```csharp
public string UserAddress { get; set; }
```

## Exemples

Montre comment utiliser le champ USERADDRESS.

```csharp
Document doc = new Document();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
UserInformation userInformation = new UserInformation();
userInformation.Address = "123 Main Street";
doc.FieldOptions.CurrentUser = userInformation;

// Créez un champ USERADDRESS pour afficher l'adresse de l'utilisateur actuel,
// extrait de l'objet UserInformation que nous avons créé ci-dessus.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserAddress fieldUserAddress = (FieldUserAddress)builder.InsertField(FieldType.FieldUserAddress, true);
Assert.AreEqual(" USERADDRESS ", fieldUserAddress.GetFieldCode());
Assert.AreEqual("123 Main Street", fieldUserAddress.Result);

// Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserAddress.UserAddress = "456 North Road";
fieldUserAddress.Update();

Assert.AreEqual(" USERADDRESS  \"456 North Road\"", fieldUserAddress.GetFieldCode());
Assert.AreEqual("456 North Road", fieldUserAddress.Result);

// Cela n'affecte pas la valeur de l'objet UserInformation.
Assert.AreEqual("123 Main Street", doc.FieldOptions.CurrentUser.Address);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERADDRESS.docx");
```

### Voir également

* class [FieldUserAddress](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
