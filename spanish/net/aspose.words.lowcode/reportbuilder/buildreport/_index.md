---
title: ReportBuilder.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: Aspose.Words para .NET
description: Cree sin esfuerzo informes personalizados con el método BuildReport de ReportBuilder, llenando su plantilla con datos para obtener resultados profesionales en todo momento.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/reportbuilder/buildreport/
---
## BuildReport(*string, string, object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_12}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| data | Object | Un objeto de fuente de datos. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo rellenar un documento con datos.

```csharp
public void BuildReportData()
{
    // Hay varias formas de rellenar un documento con datos:
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

### Ver también

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_6}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo rellenar un documento con datos.

```csharp
public void BuildReportData()
{
    // Hay varias formas de rellenar un documento con datos:
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

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_9}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales, a partir de flujos de entrada y salida.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo rellenar un documento con datos utilizando documentos de la secuencia.

```csharp
// Hay varias formas de rellenar un documento con datos utilizando documentos del flujo:
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

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_3}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales, a partir de flujos de entrada y salida.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_13}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| data | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_7}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_10}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, string dataSourceName, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_1}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_4}

Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object | Un objeto de fuente de datos. |
| dataSourceName | String | Un nombre para hacer referencia al objeto de fuente de datos en la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_14}

Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. Esta sobrecarga determina automáticamente el formato de guardado en función de la extensión del archivo de salida.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object[] data, 
    string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_8}

Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida específico y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_11}

Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida específico y opciones adicionales.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object[] data, string[] dataSourceNames, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_2}

Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con el formato de salida especificado y opciones adicionales a partir de los flujos de archivos de entrada y salida especificados.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo rellenar un documento con datos utilizando documentos de la secuencia.

```csharp
// Hay varias formas de rellenar un documento con datos utilizando documentos del flujo:
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

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_5}

Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con el formato de salida especificado y opciones adicionales a partir de los flujos de archivos de entrada y salida especificados.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| outputStream | Stream | El flujo de archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| data | Object[] | Una matriz de objetos de fuente de datos. |
| dataSourceNames | String[] | Una matriz de nombres para hacer referencia a los objetos de fuente de datos dentro de la plantilla. |
| reportBuilderOptions | ReportBuilderOptions | Opciones de creación de informes adicionales. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
