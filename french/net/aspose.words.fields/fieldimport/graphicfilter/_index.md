---
title: FieldImport.GraphicFilter
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldImport propriété. Obtient ou définit le nom du filtre pour le format du graphique à insérer.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldimport/graphicfilter/
---
## FieldImport.GraphicFilter property

Obtient ou définit le nom du filtre pour le format du graphique à insérer.

```csharp
public string GraphicFilter { get; set; }
```

### Exemples

Montre comment insérer des images à l'aide des champs IMPORT et INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Vous trouverez ci-dessous deux types de champs similaires que nous pouvons utiliser pour afficher des images liées à partir du système de fichiers local.
// 1 - Le champ INCLUDEPICTURE :
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Applique le filtre PNG32.FLT.
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
* espace de noms [Aspose.Words.Fields](../../fieldimport/)
* Assemblée [Aspose.Words](../../../)


