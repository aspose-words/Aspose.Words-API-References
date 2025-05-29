---
title: MailMergeOptions.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words pour .NET
description: Bénéficiez de fonctionnalités avancées de publipostage grâce à la propriété UseNonMergeFields. Intégrez facilement MERGEFIELD et d'autres types de champs pour une personnalisation optimisée des documents.
type: docs
weight: 130
url: /fr/net/aspose.words.lowcode/mailmergeoptions/usenonmergefields/
---
## MailMergeOptions.UseNonMergeFields property

Quand`vrai` , spécifie qu'en plus des champs MERGEFIELD, le publipostage est effectué dans certains autres types de champs et également dans les balises "{{fieldName}}".

```csharp
public bool UseNonMergeFields { get; set; }
```

## Remarques

Normalement, le publipostage s'effectue uniquement dans les champs MERGEFIELD, mais plusieurs clients ont créé leur reporting à partir d'autres champs et ont ainsi généré de nombreux documents. Afin de simplifier la migration (et parce que cette approche était utilisée indépendamment par plusieurs clients), la possibilité de fusionner avec d'autres champs a été introduite.

Quand`UseNonMergeFields` est réglé sur`vrai`Aspose.Words effectuera un publipostage dans les champs suivants :

MERGEFIELD Nom du champ

MACROBUTTON NOM MACRO Nom du champ

SI 0 = 0 "{FieldName}" ""

De plus, lorsque`UseNonMergeFields` est réglé sur`vrai`Aspose.Words effectuera un publipostage dans les balises texte "{{fieldName}}". Il ne s'agit pas de champs, mais simplement de balises texte.

### Voir également

* class [MailMergeOptions](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
