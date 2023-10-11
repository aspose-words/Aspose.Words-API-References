---
title: ReportingEngine.BuildReport
second_title: Référence de l'API Aspose.Words pour .NET
description: ReportingEngine méthode. Remplit le document modèle spécifié avec les données de la source spécifiée ce qui en fait un rapport prêt.
type: docs
weight: 40
url: /fr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un document modèle à remplir avec des données. |
| dataSource | Object | Un objet source de données. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/)la propriété inclut leInlineErrorMessages option.

### Remarques

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données dans le document modèle, mais vous ne pouvez pas référencer l'objet de la source de données lui-même. Vous devriez utiliser le`BuildReport` surcharge pour y parvenir.

Un objet source de données peut être de l'un des types suivants :

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
* Tout autre type .NET arbitraire, non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des documents modèles, consultez la référence sur la syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un document modèle à remplir avec des données. |
| dataSource | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l'objet de source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/)la propriété inclut leInlineErrorMessages option.

### Remarques

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données et l'objet de la source de données lui-même dans le modèle. Si vous ne faites pas référence à l'objet source de données lui-même, vous pouvez omettre*dataSourceName* passant`nul` ou utilisez le`BuildReport` surcharge.

Un objet source de données peut être de l'un des types suivants :

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
* Tout autre type .NET arbitraire, non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des documents modèles, consultez la référence sur la syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Remplit le document modèle spécifié avec les données des sources spécifiées, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un document modèle à remplir avec des données. |
| dataSources | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Tableau de noms pour référencer les objets de source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/)la propriété inclut leInlineErrorMessages option.

### Remarques

En utilisant cette surcharge, vous pouvez référencer plusieurs objets de source de données et leurs membres dans le modèle. Le nom de la première source de données peut être omis (c'est-à-dire être une chaîne vide ou`nul` si vous souhaitez référencer les membres de la source de données mais pas l'objet de la source de données lui-même. Les noms des autres sources de données doivent être précisés et uniques.

Si vous envisagez d'utiliser une seule source de données, envisagez d'utiliser`BuildReport` et`BuildReport` surcharge à la place.

Un objet source de données peut être de l'un des types suivants :

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
* Tout autre type .NET arbitraire, non dynamique et non anonyme

Pour plus d'informations sur l'utilisation de sources de données de différents types dans des documents modèles, consultez la référence sur la syntaxe du modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax). .

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../reportingengine/)
* Assemblée [Aspose.Words](../../../)


