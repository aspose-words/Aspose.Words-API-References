---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words pour .NET
description: Document ShadeFormData propriété. Spécifie sil faut activer lombrage gris sur les champs du formulaire en C#.
type: docs
weight: 380
url: /fr/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Spécifie s'il faut activer l'ombrage gris sur les champs du formulaire.

```csharp
public bool ShadeFormData { get; set; }
```

## Exemples

Montre comment appliquer un ombrage gris aux champs de formulaire.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Nous pouvons désactiver l'ombrage gris afin que le texte marqué par un signet se fonde dans l'autre texte.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
