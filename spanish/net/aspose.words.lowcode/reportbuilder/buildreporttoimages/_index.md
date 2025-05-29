---
title: ReportBuilder.BuildReportToImages
linktitle: BuildReportToImages
articleTitle: BuildReportToImages
second_title: Aspose.Words para .NET
description: Transforme sus documentos de plantilla sin esfuerzo con el método BuildReportToImages de ReportBuilder, combinando datos de diversas fuentes en imágenes impresionantes.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/reportbuilder/buildreporttoimages/
---
## BuildReportToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages_1}

Rellena el documento de plantilla con datos de múltiples fuentes. Representa la salida en imágenes.

```csharp
public static Stream[] BuildReportToImages(string inputFileName, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Ejemplos

Muestra cómo rellenar un documento con fuentes de datos.

```csharp
public void BuildReportDataSource()
{
    // Hay varias formas de rellenar un documento con fuentes de datos:
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

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReportToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages}

Rellena el documento de plantilla con datos de múltiples fuentes. Representa la salida en imágenes.

```csharp
public static Stream[] BuildReportToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Opciones de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Ejemplos

Muestra cómo rellenar un documento con fuentes de datos utilizando documentos de la secuencia.

```csharp
// Hay varias formas de rellenar un documento con fuentes de datos utilizando documentos de la secuencia:
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

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
