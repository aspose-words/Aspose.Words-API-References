---
title: Document.ShadeFormData
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Spécifie sil faut activer lombrage gris sur les champs de formulaire.
type: docs
weight: 360
url: /fr/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Spécifie s'il faut activer l'ombrage gris sur les champs de formulaire.

```csharp
public bool ShadeFormData { get; set; }
```

### Exemples

Montre comment appliquer un ombrage gris aux champs de formulaire.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Nous pouvons désactiver l'ombrage gris, de sorte que le texte marqué d'un signet se confond avec l'autre texte.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


