---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words pour .NET
description: Générez sans effort des rapports prêts à l'emploi avec la méthode BuildReport de ReportingEngine, en remplissant de manière transparente les modèles avec les données de la source choisie.
type: docs
weight: 50
url: /fr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSource | Object | Un objet source de données. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/) la propriété comprend leInlineErrorMessages option.

## Remarques

Grâce à cette surcharge, vous pouvez référencer les membres de la source de données dans le document modèle, mais vous ne pouvez pas référencer l'objet source de données lui-même. Vous devez utiliser la commande`BuildReport` surcharge pour y parvenir.

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
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur la façon de travailler avec des sources de données de différents types dans des documents de modèle, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Remplit le document modèle spécifié avec les données de la source spécifiée, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSource | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/) la propriété comprend leInlineErrorMessages option.

## Remarques

En utilisant cette surcharge, vous pouvez référencer les membres de la source de données et l'objet source de données lui-même dans le modèle. Si vous n'allez pas référencer l'objet source de données lui-même, vous pouvez omettre*dataSourceName* passant`nul` ou utilisez le`BuildReport` surcharge.

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
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur la façon de travailler avec des sources de données de différents types dans des documents de modèle, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Exemples

Montre comment autoriser les membres manquants.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Montre comment supprimer des paragraphes de manière sélective.

```csharp
// Le modèle contient des balises avec un point d'exclamation. Pour ces balises, les paragraphes vides seront supprimés.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Montre comment afficher les valeurs sous forme de texte en dollars.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Remplit le document modèle spécifié avec les données des sources spécifiées, ce qui en fait un rapport prêt.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| document | Document | Un modèle de document à remplir avec des données. |
| dataSources | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |

### Return_Value

Un indicateur indiquant si l'analyse du document modèle a réussi. L'indicateur renvoyé n'a de sens que si une valeur de[`Options`](../options/) la propriété comprend leInlineErrorMessages option.

## Remarques

En utilisant cette surcharge, vous pouvez référencer plusieurs objets de source de données et leurs membres dans le modèle. Le nom de la première source de données peut être omis (c'est-à-dire être une chaîne vide ou`nul` Si vous référencez les membres de la source de données, mais pas l'objet source lui-même, les noms des autres sources de données doivent être spécifiés et uniques.

Si vous envisagez d'utiliser une seule source de données, pensez à utiliser`BuildReport` et`BuildReport` surcharges à la place.

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
* Tout autre type .NET arbitraire non dynamique et non anonyme

Pour plus d'informations sur la façon de travailler avec des sources de données de différents types dans des documents de modèle, consultez la référence de syntaxe de modèle (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Exemples

Montre comment travailler avec des graphiques à partir de Word 2016.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Montre comment conserver la numérotation insérée telle quelle.

```csharp
// Par défaut, les listes numérotées d'un document modèle sont continuées lorsque leurs identifiants correspondent à ceux d'un document en cours d'insertion.
// Avec "-sourceNumbering", la numérotation doit être séparée et conservée telle quelle.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Voir également

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* espace de noms [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Assemblée [Aspose.Words](../../../)
