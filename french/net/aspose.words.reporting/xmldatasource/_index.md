---
title: XmlDataSource Class
linktitle: XmlDataSource
articleTitle: XmlDataSource
second_title: Aspose.Words pour .NET
description: Bénéficiez de rapports performants avec Aspose.Words.XmlDataSource. Accédez facilement aux données XML pour une intégration transparente à vos rapports et une meilleure visualisation des données.
type: docs
weight: 5490
url: /fr/net/aspose.words.reporting/xmldatasource/
---
## XmlDataSource class

Fournit l'accès aux données d'un fichier ou d'un flux XML à utiliser dans un rapport.

Pour en savoir plus, visitez le[Moteur de création de rapports LINQ](https://docs.aspose.com/words/net/linq-reporting-engine/) article de documentation.

```csharp
public class XmlDataSource
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [XmlDataSource](xmldatasource/#constructor)(*Stream*) | Crée une nouvelle source de données avec des données provenant d'un flux XML en utilisant les options par défaut pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_4)(*string*) | Crée une nouvelle source de données avec des données provenant d'un fichier XML en utilisant les options par défaut pour le chargement de données XML. |
| [XmlDataSource](xmldatasource/#constructor_2)(*Stream, Stream*) | Crée une source de données à partir d'un flux XML utilisant un flux de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_1)(*Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un flux XML en utilisant les options spécifiées pour le chargement de données XML. |
| [XmlDataSource](xmldatasource/#constructor_6)(*string, string*) | Crée une source de données à partir d'un fichier XML, à l'aide d'un fichier de définition de schéma XML. Les options par défaut sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_5)(*string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crée une nouvelle source de données avec des données provenant d'un fichier XML en utilisant les options spécifiées pour le chargement de données XML. |
| [XmlDataSource](xmldatasource/#constructor_3)(*Stream, Stream, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crée une source de données à partir d'un flux XML utilisant un flux de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML. |
| [XmlDataSource](xmldatasource/#constructor_7)(*string, string, [XmlDataLoadOptions](../xmldataloadoptions/)*) | Crée une source de données à partir des données d'un fichier XML, à l'aide d'un fichier de définition de schéma XML. Les options spécifiées sont utilisées pour le chargement des données XML. |

## Remarques

Pour accéder aux données du fichier ou du flux correspondant lors de la génération d'un rapport, transmettez une instance de cette classe en tant que source de données à l'un des[`ReportingEngine`](../reportingengine/) .BuildReport surcharges.

Dans les documents modèles, si un élément XML de niveau supérieur contient uniquement une liste d'éléments du même type, un`XmlDataSource` l'instance doit être traitée de la même manière que si elle était uneDataTable instance . Sinon, une`XmlDataSource` l'instance doit être traitée de la même manière que si elle était uneDataRow Instance . Pour plus d'informations, consultez la référence de syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

Lorsqu'une définition de schéma XML est transmise à un constructeur de cette classe, les types de données des valeurs des éléments XML simples et des attributs sont déterminés selon le schéma. Ainsi, dans les documents modèles, vous pouvez utiliser des valeurs typées plutôt que de simples chaînes.

Lorsque la définition de schéma XML n'est pas transmise à un constructeur de cette classe, les types de données des valeurs des éléments XML simples et des attributs sont déterminés automatiquement à partir de leurs représentations sous forme de chaîne. Ainsi, dans les documents modèles, vous pouvez également utiliser des valeurs typées. Le moteur est capable de reconnaître automatiquement les valeurs des types suivants :

* Nullable
* Nullable
* Nullable
* Nullable
* String

Notez que pour que la reconnaissance automatique des types de données fonctionne, les représentations sous forme de chaîne des valeurs des éléments XML simples et des attributs doivent être formées à l'aide de paramètres de culture invariants.

Pour remplacer le comportement par défaut du chargement des données XML, initialisez et transmettez un[`XmlDataLoadOptions`](../xmldataloadoptions/) instance d'un constructeur de cette classe.

## Exemples

Montrez comment utiliser XML comme source de données (chaîne).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

XmlDataSource dataSource = new XmlDataSource(MyDir + "List of people.xml");
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataString.docx");
```

Montrez comment utiliser XML comme source de données (flux).

```csharp
Document doc = new Document(MyDir + "Reporting engine template - XML data destination.docx");

using (FileStream stream = File.OpenRead(MyDir + "List of people.xml"))
{
    XmlDataSource dataSource = new XmlDataSource(stream);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.XmlDataStream.docx");
```

### Voir également

* espace de noms [Aspose.Words.Reporting](../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../)
