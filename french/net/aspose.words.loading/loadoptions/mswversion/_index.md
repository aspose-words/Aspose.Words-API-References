---
title: LoadOptions.MswVersion
linktitle: MswVersion
articleTitle: MswVersion
second_title: Aspose.Words pour .NET
description: Optimisez le chargement des documents avec LoadOptions MswVersion. Assurez la compatibilité avec certaines versions de MS Word, en utilisant par défaut Word 2019 pour une intégration transparente.
type: docs
weight: 100
url: /fr/net/aspose.words.loading/loadoptions/mswversion/
---
## LoadOptions.MswVersion property

Permet de spécifier que le processus de chargement du document doit correspondre à une version spécifique de MS Word. La valeur par défaut estWord2019

```csharp
public MsWordVersion MswVersion { get; set; }
```

## Remarques

Différentes versions de Word peuvent gérer certains aspects du contenu et du formatage du document légèrement différemment pendant le processus de chargement, ce qui peut entraîner des différences mineures dans le modèle d'objet de document.

## Exemples

Montre comment émuler la procédure de chargement d'une version spécifique de Microsoft Word lors du chargement du document.

```csharp
// Par défaut, Aspose.Words charge les documents conformément à la spécification Microsoft Word 2019.
LoadOptions loadOptions = new LoadOptions();

Assert.AreEqual(MsWordVersion.Word2019, loadOptions.MswVersion);

// Ce document ne dispose pas du style de formatage de paragraphe par défaut.
// Ce style par défaut sera régénéré lorsque nous chargerons le document avec Microsoft Word ou Aspose.Words.
loadOptions.MswVersion = MsWordVersion.Word2007;
Document doc = new Document(MyDir + "Document.docx", loadOptions);

// L'espacement des lignes du style aura cette valeur lorsqu'il sera chargé par la spécification Microsoft Word 2007.
Assert.AreEqual(12.95d, doc.Styles.DefaultParagraphFormat.LineSpacing, 0.01d);
```

### Voir également

* enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
