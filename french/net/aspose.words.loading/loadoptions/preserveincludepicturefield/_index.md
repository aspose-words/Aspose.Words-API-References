---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words pour .NET
description: LoadOptions PreserveIncludePictureField propriété. Obtient ou définit sil faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut estFAUX  en C#.
type: docs
weight: 120
url: /fr/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

Obtient ou définit s'il faut conserver le champ INCLUDEPICTURE lors de la lecture des formats Microsoft Word. La valeur par défaut est`FAUX` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## Remarques

Par défaut, le champ INCLUDEPICTURE est converti en objet forme. Vous pouvez remplacer cela si vous avez besoin que le champ soit préservé, par exemple, si vous souhaitez le mettre à jour par programme. Notez cependant que l'approche this n'est pas courante pour Aspose.Words. Utilisez-le à vos propres risques.

L'un des cas d'utilisation possibles peut consister à utiliser un MERGEFIELD comme champ enfant pour modifier dynamiquement le chemin source de l'image. Dans ce cas, vous devez conserver INCLUDEPICTURE dans le modèle.

## Exemples

Montre comment conserver ou supprimer les champs INCLUDEPICTURE lors du chargement d’un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Nous pouvons définir un indicateur dans un objet LoadOptions pour décider s'il faut convertir tous les champs INCLUDEPICTURE
    // dans les formes d'image lors du chargement d'un document qui les contient.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
