---
title: ReportBuildOptions Enum
linktitle: ReportBuildOptions
articleTitle: ReportBuildOptions
second_title: Aspose.Words pour .NET
description: Aspose.Words.Reporting.ReportBuildOptions énumération. Spécifie les options contrôlant le comportement deReportingEngine lors de la création dun rapport en C#.
type: docs
weight: 4720
url: /fr/net/aspose.words.reporting/reportbuildoptions/
---
## ReportBuildOptions enumeration

Spécifie les options contrôlant le comportement de[`ReportingEngine`](../reportingengine/) lors de la création d'un rapport.

```csharp
[Flags]
public enum ReportBuildOptions
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Spécifie les options par défaut. |
| AllowMissingMembers | `1` | Spécifie que les membres d'objet manquants doivent être traités comme des littéraux nuls par le moteur. Cette option affecte uniquement l'accès aux membres d'objet d'instance (c'est-à-dire non statiques) et aux méthodes d'extension. Si cette option n'est pas définie, le moteur lève une exception lorsqu'il rencontre un membre d'objet manquant. |
| RemoveEmptyParagraphs | `2` | Spécifie que le moteur doit supprimer les paragraphes devenus vides une fois que les balises de syntaxe du modèle ont été supprimées ou remplacées par des valeurs vides. |
| InlineErrorMessages | `4` | Spécifie que le moteur doit intégrer les messages d'erreur de syntaxe du modèle dans les documents de sortie. Si cette option n'est pas définie, le moteur lève une exception lorsqu'il rencontre une erreur de syntaxe. |
| UseLegacyHeaderFooterVisiting | `8` | Spécifie que le moteur doit visiter les nœuds enfants de section (en-têtes, pieds de page, corps) dans un ordre compatible avec les versions Aspose.Words antérieures à 21.9. |
| RespectJpegExifOrientation | `10` | Spécifie que le moteur doit utiliser les valeurs d'orientation de l'image EXIF ​​​​pour faire pivoter de manière appropriée les images JPEG insérées . |

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
