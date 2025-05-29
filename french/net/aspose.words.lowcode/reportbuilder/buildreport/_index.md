---
title: ReportBuilder.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words pour .NET
description: Créez sans effort des rapports personnalisés avec la méthode BuildReport de ReportBuilder, en remplissant votre modèle avec des données pour des résultats professionnels à chaque fois.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/reportbuilder/buildreport/
---
## BuildReport(*string, string, object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_12}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| data | Object | Un objet source de données. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des données.

```csharp
public void BuildReportData()
{
    // Il existe plusieurs façons de remplir un document avec des données :
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Voir également

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_6}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des données.

```csharp
public void BuildReportData()
{
    // Il existe plusieurs façons de remplir un document avec des données :
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_9}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires, à partir des flux d'entrée et de sortie.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment remplir un document avec des données à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons de remplir un document avec des données à l'aide de documents provenant du flux :
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_3}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires, à partir des flux d'entrée et de sortie.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_13}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| data | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des sources de données.

```csharp
public void BuildReportDataSource()
{
    // Il existe plusieurs façons de remplir un document avec des sources de données :
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Voir également

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_7}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié, une référence de source de données nommée et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des sources de données.

```csharp
public void BuildReportDataSource()
{
    // Il existe plusieurs façons de remplir un document avec des sources de données :
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_10}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié, une référence de source de données nommée et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, string dataSourceName, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_1}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment remplir un document avec des sources de données à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons de remplir un document avec des sources de données à l'aide de documents du flux :
MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

using (FileStream streamIn = new FileStream(MyDir + "Report building.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" });

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.4.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.Create(reportBuilderContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_4}

Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object | Un objet source de données. |
| dataSourceName | String | Un nom pour référencer l’objet source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_14}

Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport complet avec des options supplémentaires. Cette surcharge détermine automatiquement le format d'enregistrement en fonction de l'extension du fichier de sortie.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object[] data, 
    string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| data | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des sources de données.

```csharp
public void BuildReportDataSource()
{
    // Il existe plusieurs façons de remplir un document avec des sources de données :
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Voir également

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_8}

Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec un format de sortie spécifié et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

## Exemples

Montre comment remplir un document avec des sources de données.

```csharp
public void BuildReportDataSource()
{
    // Il existe plusieurs façons de remplir un document avec des sources de données :
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_11}

Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec un format de sortie spécifié et des options supplémentaires.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object[] data, string[] dataSourceNames, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFileName | String | Le nom du fichier d'entrée. |
| outputFileName | String | Le nom du fichier de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page sera enregistrée dans un fichier distinct. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichier de chaque partie, conformément à la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_2}

Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires à partir des flux de fichiers d'entrée et de sortie spécifiés.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveFormat | SaveFormat | Le format de sauvegarde de la sortie. |
| data | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

## Exemples

Montre comment remplir un document avec des données à l'aide de documents du flux.

```csharp
// Il existe plusieurs façons de remplir un document avec des données à l'aide de documents provenant du flux :
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_5}

Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires à partir des flux de fichiers d'entrée et de sortie spécifiés.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStream | Stream | Le flux du fichier d'entrée. |
| outputStream | Stream | Le flux de fichiers de sortie. |
| saveOptions | SaveOptions | Les options de sauvegarde de la sortie. |
| data | Object[] | Un tableau d’objets de source de données. |
| dataSourceNames | String[] | Un tableau de noms pour référencer les objets de source de données dans le modèle. |
| reportBuilderOptions | ReportBuilderOptions | Options de création de rapports supplémentaires. |

## Remarques

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée sous la forme d'un seul fichier TIFF multi-images dans le flux spécifié.

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
