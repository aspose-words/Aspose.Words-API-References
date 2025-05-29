---
title: Converter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Cree una nueva instancia del procesador del convertidor sin esfuerzo con nuestro poderoso método Converter Create para una transformación de datos perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.lowcode/converter/create/
---
## Create() {#create}

Crea una nueva instancia del procesador del convertidor.

```csharp
public static Converter Create()
```

### Ver también

* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Create(*[ConverterContext](../../convertercontext/)*) {#create_1}

Crea una nueva instancia del procesador del convertidor.

```csharp
public static Converter Create(ConverterContext context)
```

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

### Ver también

* class [ConverterContext](../../convertercontext/)
* class [Converter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
