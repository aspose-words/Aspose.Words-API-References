---
title: FieldUserInitials.UserInitials
linktitle: UserInitials
articleTitle: UserInitials
second_title: Aspose.Words pour .NET
description: Accédez et personnalisez la propriété FieldUserInitials pour gérer sans effort les initiales des utilisateurs, améliorant ainsi la personnalisation et l'expérience utilisateur.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fielduserinitials/userinitials/
---
## FieldUserInitials.UserInitials property

Obtient ou définit les initiales de l'utilisateur actuel.

```csharp
public string UserInitials { get; set; }
```

## Exemples

Montre comment utiliser le champ USERINITIALS.

```csharp
Document doc = new Document();

// Créez un objet UserInformation et définissez-le comme source d'informations utilisateur pour tous les champs que nous créons.
UserInformation userInformation = new UserInformation();
userInformation.Initials = "J. D.";
doc.FieldOptions.CurrentUser = userInformation;

// Créez un champ USERINITIALS pour afficher les initiales de l'utilisateur actuel,
// extrait de l'objet UserInformation que nous avons créé ci-dessus.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldUserInitials fieldUserInitials = (FieldUserInitials)builder.InsertField(FieldType.FieldUserInitials, true);
Assert.AreEqual(userInformation.Initials, fieldUserInitials.Result);

Assert.AreEqual(" USERINITIALS ", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. D.", fieldUserInitials.Result);

 // Nous pouvons définir cette propriété pour que notre champ remplace la valeur actuellement stockée dans l'objet UserInformation.
fieldUserInitials.UserInitials = "J. C.";
fieldUserInitials.Update();

Assert.AreEqual(" USERINITIALS  \"J. C.\"", fieldUserInitials.GetFieldCode());
Assert.AreEqual("J. C.", fieldUserInitials.Result);

// Cela n'affecte pas la valeur de l'objet UserInformation.
Assert.AreEqual("J. D.", doc.FieldOptions.CurrentUser.Initials);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.USERINITIALS.docx");
```

### Voir également

* class [FieldUserInitials](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
