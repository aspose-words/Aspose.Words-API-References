---
title: Field.GetFieldCode
linktitle: GetFieldCode
articleTitle: GetFieldCode
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetFieldCode pour récupérer facilement le texte entre le début et le séparateur des champs, y compris les codes et les résultats des champs enfants. Améliorez votre efficacité de codage !
type: docs
weight: 110
url: /fr/net/aspose.words.fields/field/getfieldcode/
---
## GetFieldCode() {#getfieldcode}

Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur). Le code du champ et le résultat du champ des champs enfants sont inclus.

```csharp
public string GetFieldCode()
```

## Exemples

Montre comment insérer un champ dans un document à l'aide d'un code de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Cette surcharge de la méthode InsertField met automatiquement à jour les champs insérés.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

Montre comment obtenir le code de champ d'un champ.

```csharp
// Ouvrez un document qui contient un MERGEFIELD à l'intérieur d'un champ IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Il existe deux manières d'obtenir le code de champ d'un champ :
// 1 - Omettre ses champs internes :
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inclure ses champs internes :
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Par défaut, la méthode GetFieldCode affiche les champs internes.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)

---

## GetFieldCode(*bool*) {#getfieldcode_1}

Renvoie le texte entre le début du champ et le séparateur de champ (ou la fin du champ s'il n'y a pas de séparateur).

```csharp
public string GetFieldCode(bool includeChildFieldCodes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| includeChildFieldCodes | Boolean | `vrai` si les codes des champs enfants doivent être inclus. |

## Exemples

Montre comment obtenir le code de champ d'un champ.

```csharp
// Ouvrez un document qui contient un MERGEFIELD à l'intérieur d'un champ IF.
Document doc = new Document(MyDir + "Nested fields.docx");
FieldIf fieldIf = (FieldIf)doc.Range.Fields[0];

// Il existe deux manières d'obtenir le code de champ d'un champ :
// 1 - Omettre ses champs internes :
Assert.AreEqual(" IF  > 0 \" (surplus of ) \" \"\" ", fieldIf.GetFieldCode(false));

// 2 - Inclure ses champs internes :
Assert.AreEqual($" IF \u0013 MERGEFIELD NetIncome \u0014\u0015 > 0 \" (surplus of \u0013 MERGEFIELD  NetIncome \\f $ \u0014\u0015) \" \"\" ",
    fieldIf.GetFieldCode(true));

// Par défaut, la méthode GetFieldCode affiche les champs internes.
Assert.AreEqual(fieldIf.GetFieldCode(), fieldIf.GetFieldCode(true));
```

### Voir également

* class [Field](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
