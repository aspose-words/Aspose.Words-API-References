---
title: FieldOptions.IsBidiTextSupportedOnUpdate
linktitle: IsBidiTextSupportedOnUpdate
articleTitle: IsBidiTextSupportedOnUpdate
second_title: Aspose.Words pour .NET
description: FieldOptions IsBidiTextSupportedOnUpdate propriété. Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non en C#.
type: docs
weight: 150
url: /fr/net/aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/
---
## FieldOptions.IsBidiTextSupportedOnUpdate property

Obtient ou définit la valeur indiquant si le texte bidirectionnel est entièrement pris en charge lors de la mise à jour du champ ou non.

```csharp
public bool IsBidiTextSupportedOnUpdate { get; set; }
```

## Remarques

Lorsque cette propriété est définie sur`vrai`, des étapes supplémentaires sont effectuées pour produire un résultat de champ compatible avec la langue de droite à gauche (c'est-à-dire l'arabe ou l'hébreu) lors de sa mise à jour.

Lorsque cette propriété est définie sur`FAUX` et le langage de droite à gauche est utilisé, l'exactitude du champ result après sa mise à jour n'est pas garantie.

La valeur par défaut est`FAUX`.

## Exemples

Montre comment utiliser FieldOptions pour garantir que la mise à jour des champs prend entièrement en charge le texte bidirectionnel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Assurez-vous que toute opération de champ impliquant du texte de droite à gauche s'effectue comme prévu.
doc.FieldOptions.IsBidiTextSupportedOnUpdate = true;

// Utilisez un générateur de documents pour insérer un champ contenant le texte de droite à gauche.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים" }, 0);
comboBox.CalculateOnExit = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.Bidi.docx");
```

### Voir également

* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
