---
title: FieldUserName.UserName
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldUserName propriété. Gest ou définit le nom de lutilisateur actuel.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldusername/username/
---
## FieldUserName.UserName property

Gest ou définit le nom de l'utilisateur actuel.

```csharp
public string UserName { get; set; }
```

### Exemples

Montre comment utiliser le champ USERNAME.

```csharp
Document doc = new Document();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
UserInformation userInformation = new UserInformation();
userInformation.Name = "John Doe";
doc.FieldOptions.CurrentUser = userInformation;

DocumentBuilder builder = new DocumentBuilder(doc);

// Crée un champ USERNAME pour afficher le nom de l'utilisateur courant,
// tiré de l'objet UserInformation que nous avons créé ci-dessus.
FieldUserName fieldUserName = (FieldUserName)builder.InsertField(FieldType.FieldUserName, true);
Assert.AreEqual(userInformation.Name, fieldUserName.Result);

Assert.AreEqual(" USERNAME ", fieldUserName.GetFieldCode());
Assert.AreEqual("John Doe", fieldUserName.Result);

 // Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserName.UserName = "Jane Doe";
fieldUserName.Update();

Assert.AreEqual(" USERNAME  \"Jane Doe\"", fieldUserName.GetFieldCode());
Assert.AreEqual("Jane Doe", fieldUserName.Result);

// Cela n'affecte pas la valeur de l'objet UserInformation.
Assert.AreEqual("John Doe", doc.FieldOptions.CurrentUser.Name);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERNAME.docx");
```

### Voir également

* class [FieldUserName](../)
* espace de noms [Aspose.Words.Fields](../../fieldusername/)
* Assemblée [Aspose.Words](../../../)


