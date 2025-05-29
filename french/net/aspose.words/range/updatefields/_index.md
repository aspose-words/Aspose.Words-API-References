---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words pour .NET
description: Améliorez vos documents sans effort avec la méthode Range UpdateFields, en mettant à jour les valeurs des champs rapidement et efficacement pour une précision améliorée.
type: docs
weight: 130
url: /fr/net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Met à jour les valeurs des champs de document dans cette plage.

```csharp
public void UpdateFields()
```

## Remarques

Lorsque vous ouvrez, modifiez puis enregistrez un document, Aspose.Words ne met pas à jour les champs automatiquement, il les conserve intacts. Par conséquent, vous souhaiterez généralement appeler cette méthode avant d'enregistrer si vous avez modifié le document par programmation et que vous souhaitez vous assurer que les valeurs de champ appropriées (calculées) apparaissent dans le document enregistré.

Il n'est pas nécessaire de mettre à jour les champs après l'exécution d'un publipostage, car le publipostage est une sorte de field update et met automatiquement à jour tous les champs du document.

Cette méthode ne met pas à jour tous les types de champs. Pour la liste détaillée des types de champs pris en charge, consultez le Guide du programmeur.

Cette méthode ne met pas à jour les champs liés aux algorithmes de mise en page (par exemple PAGE, PAGES, PAGEREF). Les champs liés à la mise en page sont mis à jour lorsque vous affichez un document ou appelez[`UpdatePageLayout`](../../document/updatepagelayout/).

Pour mettre à jour les champs dans l'ensemble du document, utilisez[`UpdateFields`](../../document/updatefields/).

## Exemples

Montre comment mettre à jour tous les champs d'une plage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// Les champs DOCPROPERTY ci-dessus afficheront la valeur de cette propriété de document intégrée.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// Si nous mettons à jour la valeur d'une propriété de document, nous devrons mettre à jour tous les champs DOCPROPERTY pour l'afficher.
Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

// Mettre à jour tous les champs qui se trouvent dans la plage de la première section.
doc.FirstSection.Range.UpdateFields();

Assert.AreEqual("MyCategory", doc.Range.Fields[0].Result);
Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
