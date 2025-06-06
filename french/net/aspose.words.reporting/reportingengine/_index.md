---
title: ReportingEngine Class
linktitle: ReportingEngine
articleTitle: ReportingEngine
second_title: Aspose.Words pour .NET
description: Bénéficiez d'une puissante automatisation documentaire avec Aspose.Words.ReportingEngine. Remplissez facilement vos modèles avec des données et personnalisez vos paramètres pour des rapports fluides.
type: docs
weight: 5470
url: /fr/net/aspose.words.reporting/reportingengine/
---
## ReportingEngine class

Fournit des routines pour remplir les documents modèles avec des données et un ensemble de paramètres pour contrôler ces routines.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class ReportingEngine
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ReportingEngine](reportingengine/)() | Initialise une nouvelle instance de cette classe. |

## Propriétés

| Nom | La description |
| --- | --- |
| [KnownTypes](../../aspose.words.reporting/reportingengine/knowntypes/) { get; } | Obtient un ensemble non ordonné (c'est-à-dire une collection d'éléments uniques) contenantType objets dont les noms entièrement ou partiellement qualifiés peuvent être utilisés dans les modèles de rapport traités par cette instance engine pour appeler les membres statiques des types correspondants, effectuer des conversions de types, etc. |
| [MissingMemberMessage](../../aspose.words.reporting/reportingengine/missingmembermessage/) { get; set; } | Obtient ou définit une valeur de chaîne affichée à la place d'une expression de modèle représentant une simple référence à un membre manquant d'un objet. La valeur par défaut est une chaîne vide. |
| [Options](../../aspose.words.reporting/reportingengine/options/) { get; set; } | Obtient ou définit un ensemble d'indicateurs contrôlant le comportement de ceci`ReportingEngine` instance lors de la création d'un rapport. |
| static [UseReflectionOptimization](../../aspose.words.reporting/reportingengine/usereflectionoptimization/) { get; set; } | Obtient ou définit une valeur indiquant si les appels de membres de type personnalisé effectués via l'API de réflexion sont optimisés par la génération de classes dynamiques ou non. La valeur par défaut est`vrai` . |

## Méthodes

| Nom | La description |
| --- | --- |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport)(*[Document](../../aspose.words/document/), object*) | Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_1)(*[Document](../../aspose.words/document/), object, string*) | Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt. |
| [BuildReport](../../aspose.words.reporting/reportingengine/buildreport/#buildreport_2)(*[Document](../../aspose.words/document/), object[], string[]*) | Remplit le document modèle spécifié avec les données des sources spécifiées, ce qui en fait un rapport prêt. |
| static [GetRestrictedTypes](../../aspose.words.reporting/reportingengine/getrestrictedtypes/)() | Renvoie les types, les membres ainsi que les membres des types dérivés qui doivent être inaccessibles par le moteur via la syntaxe du modèle. |
| static [SetRestrictedTypes](../../aspose.words.reporting/reportingengine/setrestrictedtypes/)(*params Type[]*) | Spécifie les types, les membres ainsi que les membres des types dérivés qui doivent être inaccessibles par le moteur via la syntaxe du modèle. |

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
