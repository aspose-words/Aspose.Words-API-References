---
title: ReportingEngine.BuildReport
second_title: Référence de l'API Aspose.Words pour .NET
description: ReportingEngine méthode. Remplit le modèle de document spécifié avec les données de la source spécifiée ce qui en fait un rapport prêt.
type: docs
weight: 40
url: /fr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Remplit le modèle de document spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSource | Object | Un objet source de données. |

### Return_Value

Un indicateur indiquant si l'analyse du modèle de document a réussi. L'indicateur renvoyé n'a de sens que si une valeur du[`Options`](../options/)propriété comprend leInlineErrorMessages option.

### Remarques

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données dans le modèle de document, mais vous ne pouvez pas référencer l'objet de source de données lui-même. Vous devriez utiliser le`BuildReport` surcharge pour y parvenir.

Un objet de source de données peut être de l'un des types suivants :

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des modèles de documents, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Remplit le modèle de document spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSource | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l'objet de source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du modèle de document a réussi. L'indicateur renvoyé n'a de sens que si une valeur du[`Options`](../options/)propriété comprend leInlineErrorMessages option.

### Remarques

À l'aide de cette surcharge, vous pouvez référencer les membres de la source de données et l'objet de la source de données lui-même dans le modèle. Si vous n'allez pas référencer l'objet source de données lui-même, vous pouvez omettre*dataSourceName* passant null ou utilisez le`BuildReport` surcharge.

Un objet de source de données peut être de l'un des types suivants :

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des modèles de documents, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Remplit le modèle de document spécifié avec des données provenant des sources spécifiées, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSources | Object[] | Un tableau d'objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du modèle de document a réussi. L'indicateur renvoyé n'a de sens que si une valeur du[`Options`](../options/)propriété comprend leInlineErrorMessages option.

### Remarques

À l'aide de cette surcharge, vous pouvez référencer plusieurs objets de source de données et leurs membres dans le modèle. Le nom de la première source de données peut être omis (c'est-à-dire être une chaîne vide ou null) si vous allez référencer les membres de la source de données mais pas l'objet source de données lui-même. Les noms des autres sources de données doivent être spécifiés et uniques.

Si vous prévoyez d'utiliser une seule source de données, envisagez d'utiliser`BuildReport` et`BuildReport` surcharges à la place.

Un objet de source de données peut être de l'un des types suivants :

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des modèles de documents, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)


