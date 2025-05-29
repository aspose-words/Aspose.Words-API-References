---
title: FieldImport.IsLinked
linktitle: IsLinked
articleTitle: IsLinked
second_title: Aspose.Words pour .NET
description: Optimisez vos documents grâce à la propriété IsLinked de FieldImport pour réduire la taille des fichiers en excluant les données graphiques. Améliorez votre efficacité et vos performances dès aujourd'hui !
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldimport/islinked/
---
## FieldImport.IsLinked property

Obtient ou définit s'il faut réduire la taille du fichier en ne stockant pas de données graphiques avec le document.

```csharp
public bool IsLinked { get; set; }
```

## Exemples

Montre comment insérer des images à l'aide des champs IMPORT et INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types de champs similaires que nous pouvons utiliser pour afficher des images liées à partir du système de fichiers local.
// 1 - Le champ INCLUDEPICTURE :
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Appliquer le filtre PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - Le champ IMPORT :
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Voir également

* class [FieldImport](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
