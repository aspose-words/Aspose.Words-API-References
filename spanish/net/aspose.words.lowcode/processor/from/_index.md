---
title: Processor.From
linktitle: From
articleTitle: From
second_title: Aspose.Words para .NET
description: Mejore su flujo de trabajo con nuestro procesador que maneja eficientemente los documentos de entrada para un procesamiento perfecto y una productividad mejorada.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/processor/from/
---
## From(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from_1}

Especifica el documento de entrada para su procesamiento.

```csharp
public Processor From(string input, LoadOptions loadOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| input | String | Nombre del archivo del documento de entrada. |
| loadOptions | LoadOptions | Opciones de carga opcionales utilizadas para cargar el documento. |

### Valor_devuelto

Devuelve el procesador con el archivo de entrada especificado.

## Observaciones

Si el procesador solo acepta un archivo como entrada, solo se procesará el último archivo especificado. [`Merger`](../../merger/) El procesador acepta varios archivos como entrada, como resultado se fusionarán todos los documentos especificados. [`Converter`](../../converter/) El procesador solo acepta un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

## Ejemplos

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

Muestra cómo fusionar documentos en un único documento de salida utilizando el contexto.

```csharp
//Hay varias formas de fusionar documentos:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## From(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#from}

Especifica el documento de entrada para su procesamiento.

```csharp
public Processor From(Stream input, LoadOptions loadOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| input | Stream | Flujo de documento de entrada. |
| loadOptions | LoadOptions | Opciones de carga opcionales utilizadas para cargar el documento. |

### Valor_devuelto

Devuelve el procesador con el flujo de archivo de entrada especificado.

## Observaciones

Si el procesador solo acepta un archivo como entrada, solo se procesará el último archivo especificado. [`Merger`](../../merger/) El procesador acepta varios archivos como entrada, como resultado se fusionarán todos los documentos especificados. [`Converter`](../../converter/) El procesador solo acepta un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

## Ejemplos

Muestra cómo convertir documentos de una secuencia con una sola línea de código usando el contexto.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

Muestra cómo fusionar documentos de una secuencia en un único documento de salida usando el contexto.

```csharp
//Hay varias formas de fusionar documentos:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Ver también

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [Processor](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
