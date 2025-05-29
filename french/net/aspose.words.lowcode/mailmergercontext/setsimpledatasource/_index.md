---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words pour .NET
description: Améliorez l'efficacité de votre publipostage avec la méthode MailMergerContext SetSimpleDataSource, simplifiant la configuration de la source de données pour une exécution transparente.
type: docs
weight: 40
url: /fr/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Définit la source de données utilisée pour exécuter un simple publipostage.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Remarques

Si la source de données de publipostage simple et la source de données pour le publipostage avec régions sont spécifiées, le publipostage avec régions est exécuté en premier, puis le publipostage simple est exécuté.

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Montre comment effectuer une opération de publipostage pour un seul enregistrement du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à l'aide de documents du flux :
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [MailMergerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Définit la source de données utilisée pour exécuter un simple publipostage.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Remarques

Si la source de données de publipostage simple et la source de données pour le publipostage avec régions sont spécifiées, le publipostage avec régions est exécuté en premier, puis le publipostage simple est exécuté.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataRow à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Montre comment effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [MailMergerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Définit la source de données utilisée pour exécuter un simple publipostage.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Remarques

Si la source de données de publipostage simple et la source de données pour le publipostage avec régions sont spécifiées, le publipostage avec régions est exécuté en premier, puis le publipostage simple est exécuté.

## Exemples

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'une table de données :
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataTable en utilisant des documents du flux :
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [MailMergerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
