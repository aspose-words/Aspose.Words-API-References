---
title: Class XmlDataSource
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Reporting.XmlDataSource classe. Fournit un accès aux données dun fichier ou dun flux XML à utiliser dans un rapport.
type: docs
weight: 4750
url: /fr/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Fournit un accès aux données d'un fichier ou d'un flux XML à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de reporting LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article documentaire.

```csharp
public class XmlDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(Stream) | Crée une nouvelle source de données avec les données d'un flux XML à l'aide des options par défaut pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(string) | Crée une nouvelle source de données avec les données d'un fichier XML en utilisant les options par défaut pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(Stream, Stream) | Crée une nouvelle source de données avec les données d'un flux XML à l'aide d'un flux de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(Stream, XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un flux XML à l'aide des options spécifiées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(string, string) | Crée une nouvelle source de données avec les données d'un fichier XML à l'aide d'un fichier de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(string, XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier XML à l'aide des options spécifiées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(Stream, Stream, XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un flux XML à l'aide d'un flux de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(string, string, XmlDataLoadOptions) | Crée une nouvelle source de données avec les données d'un fichier XML à l'aide d'un fichier de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML. |

### Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que une source de données à l'une des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, si un élément XML de niveau supérieur contient uniquement une liste d'éléments du même type, un`XmlDataSource` instance doit être traitée de la même manière que s'il s'agissait de unDataTable instance . Sinon, un`XmlDataSource` instance doit être traitée de la même manière que s'il s'agissait de unDataRow instance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

Lorsque la définition de schéma XML est transmise à un constructeur de cette classe, les types de données des valeurs des éléments XML simples et les attributs sont déterminés en fonction du schéma. Ainsi, dans les documents modèles, vous pouvez travailler avec des valeurs saisies plutôt qu'avec de simples chaînes.

Lorsque la définition de schéma XML n'est pas transmise à un constructeur de cette classe, les types de données des valeurs des éléments XML simples et les attributs sont déterminés automatiquement en fonction de leurs représentations sous forme de chaîne. Ainsi, dans les documents modèles, vous pouvez également travailler avec des valeurs saisies dans ce cas. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Notez que pour que la reconnaissance automatique des types de données fonctionne, les représentations sous forme de chaîne des valeurs des éléments XML simples et des attributs doivent être formées à l'aide de paramètres de culture invariants.

Pour remplacer le comportement par défaut du chargement des données XML, initialisez et transmettez un[`XmlDataLoadOptions`](../xmldataloadoptions/) instance à un constructeur de cette classe.

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)


