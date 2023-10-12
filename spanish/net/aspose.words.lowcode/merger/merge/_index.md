---
title: Merger.Merge
second_title: Referencia de API de Aspose.Words para .NET
description: Merger método. Combina los documentos de entrada proporcionados en un único documento de salida utilizando nombres de archivos de entrada y salida especificados.
type: docs
weight: 10
url: /es/net/aspose.words.lowcode/merger/merge/
---
## Merge(string, string[]) {#merge_4}

Combina los documentos de entrada proporcionados en un único documento de salida utilizando nombres de archivos de entrada y salida especificados.

```csharp
public static void Merge(string outputFile, string[] inputFiles)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputFile | String | El nombre del archivo de salida. |
| inputFiles | String[] | Los nombres de los archivos de entrada. |

### Observaciones

Por defectoKeepSourceFormatting se utiliza.

### Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ver también

* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(string, string[], SaveFormat, MergeFormatMode) {#merge_5}

Combina los documentos de entrada proporcionados en un único documento de salida utilizando nombres de archivos de entrada y salida especificados y el formato del documento final.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveFormat saveFormat, 
    MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputFile | String | El nombre del archivo de salida. |
| inputFiles | String[] | Los nombres de los archivos de entrada. |
| saveFormat | SaveFormat | El formato de guardado. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(string, string[], SaveOptions, MergeFormatMode) {#merge_6}

Combina los documentos de entrada proporcionados en un único documento de salida utilizando nombres de archivos de entrada y salida especificados y opciones de guardado.

```csharp
public static void Merge(string outputFile, string[] inputFiles, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputFile | String | El nombre del archivo de salida. |
| inputFiles | String[] | Los nombres de los archivos de entrada. |
| saveOptions | SaveOptions | Las opciones de guardar. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(string[], MergeFormatMode) {#merge_1}

Fusiona los documentos de entrada proporcionados en un solo documento y devuelve[`Document`](../../../aspose.words/document/) instancia del documento final.

```csharp
public static Document Merge(string[] inputFiles, MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFiles | String[] | Los nombres de los archivos de entrada. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SimpleMerge.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" });

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveOptions.docx", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.SaveFormat.pdf", new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

Document doc = Merger.Merge(new[] { MyDir + "Big document.docx", MyDir + "Tables.docx" }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.DocumentInstance.docx");
```

### Ver también

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveFormat) {#merge_2}

Combina los documentos de entrada proporcionados en un único documento de salida utilizando flujos de entrada y salida específicos y el formato del documento final.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputStream | Stream | El flujo de salida. |
| inputStreams | Stream[] | Los flujos de entrada. |
| saveFormat | SaveFormat | El formato de guardado. |

### Ejemplos

Muestra cómo fusionar documentos de la secuencia en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos desde una secuencia:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(Stream, Stream[], SaveOptions, MergeFormatMode) {#merge_3}

Combina los documentos de entrada proporcionados en un único documento de salida utilizando flujos de entrada y salida específicos y opciones de guardado.

```csharp
public static void Merge(Stream outputStream, Stream[] inputStreams, SaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| outputStream | Stream | El flujo de salida. |
| inputStreams | Stream[] | Los flujos de entrada. |
| saveOptions | SaveOptions | Las opciones de guardar. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ejemplos

Muestra cómo fusionar documentos de la secuencia en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos desde una secuencia:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)

---

## Merge(Stream[], MergeFormatMode) {#merge}

Fusiona los documentos de entrada proporcionados en un solo documento y devuelve[`Document`](../../../aspose.words/document/) instancia del documento final.

```csharp
public static Document Merge(Stream[] inputStreams, MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStreams | Stream[] | Los flujos de entrada. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ejemplos

Muestra cómo fusionar documentos de la secuencia en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos desde una secuencia:
using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveOptions.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, new OoxmlSaveOptions() { Password = "Aspose.Words" }, MergeFormatMode.KeepSourceFormatting);

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamDocument.SaveFormat.docx", FileMode.Create, FileAccess.ReadWrite))                    
            Merger.Merge(streamOut, new[] { firstStreamIn, secondStreamIn }, SaveFormat.Docx);

        Document doc = Merger.Merge(new[] { firstStreamIn, secondStreamIn }, MergeFormatMode.MergeFormatting);
        doc.Save(ArtifactsDir + "LowCode.MergeStreamDocument.DocumentInstance.docx");
    }
}
```

### Ver también

* class [Document](../../../aspose.words/document/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../merger/)
* asamblea [Aspose.Words](../../../)


