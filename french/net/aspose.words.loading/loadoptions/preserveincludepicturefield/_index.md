---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words pour .NET
description: Contrôlez le champ INCLUDEPICTURE dans les formats Microsoft Word avec LoadOptions PreserveIncludePictureField. Gérez facilement la mise en forme de vos documents pour des résultats optimaux.
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

Par défaut, le champ INCLUDEPICTURE est converti en objet forme. Vous pouvez contourner ce paramètre si vous souhaitez conserver le champ, par exemple pour le mettre à jour par programmation. Notez cependant que cette approche n'est pas courante pour Aspose.Words. Utilisez-la à vos risques et périls.

L'un des cas d'utilisation possibles consiste à utiliser un champ MERGEFIELD comme champ enfant pour modifier dynamiquement le chemin source de l'image. Dans ce cas, l'élément INCLUDEPICTURE doit être conservé dans le modèle.

## Exemples

Montre comment conserver ou supprimer les champs INCLUDEPICTURE lors du chargement d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // Nous pouvons définir un indicateur dans un objet LoadOptions pour décider de convertir ou non tous les champs INCLUDEPICTURE
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
