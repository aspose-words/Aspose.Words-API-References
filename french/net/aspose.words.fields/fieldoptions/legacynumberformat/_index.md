---
title: FieldOptions.LegacyNumberFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldOptions propriété. Obtient ou définit la valeur indiquant si le format numérique existant antérieur à AW 13.10 pour les champs est activé ou non.
type: docs
weight: 160
url: /fr/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

Obtient ou définit la valeur indiquant si le format numérique existant (antérieur à AW 13.10) pour les champs est activé ou non.

```csharp
public bool LegacyNumberFormat { get; set; }
```

### Remarques

Lorsque cette propriété est définie sur`vrai`, le symbole de modèle "#" fonctionnait comme dans .net: Remplace le signe dièse par le chiffre correspondant s'il en est un ; sinon, aucun symbole n'apparaît dans la chaîne de résultat.

Lorsque cette propriété est définie sur`FAUX`, le symbole de modèle « # » fonctionne comme MS Word : Cet élément de format spécifie les emplacements numériques requis à afficher dans le résultat. Si le résultat n'inclut pas de chiffre à cet endroit, MS Word affiche un espace. Par exemple, { = 9 + 6 \# $### } affiche 15 $.

La valeur par défaut est`FAUX`.

### Exemples

Montre comment activer le formatage des nombres hérité pour les champs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../fieldoptions/)
* Assemblée [Aspose.Words](../../../)


