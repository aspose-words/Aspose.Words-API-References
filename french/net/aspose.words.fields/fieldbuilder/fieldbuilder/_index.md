---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words pour .NET
description: Découvrez FieldBuilder, l'outil puissant pour créer et gérer facilement les champs de vos projets. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Initialise une instance du[`FieldBuilder`](../) classe.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fieldType | FieldType | Le type de terrain à construire. |

## Exemples

Montre comment créer et insérer un champ à l'aide d'un générateur de champs.

```csharp
Document doc = new Document();

// Un moyen pratique d'ajouter du contenu textuel à un document est d'utiliser un générateur de documents.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Les champs ont leur générateur, que nous pouvons utiliser pour construire un code de champ morceau par morceau.
// Dans ce cas, nous allons construire un champ BARCODE représentant un code postal américain,
// puis insérez-le devant un Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Voir également

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
