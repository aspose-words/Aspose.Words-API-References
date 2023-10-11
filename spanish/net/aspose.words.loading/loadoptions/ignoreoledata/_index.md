---
title: LoadOptions.IgnoreOleData
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions propiedad. Especifica si se ignoran los datos OLE.
type: docs
weight: 70
url: /es/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Especifica si se ignoran los datos OLE.

```csharp
public bool IgnoreOleData { get; set; }
```

### Observaciones

Ignorar los datos OLE puede reducir el consumo de memoria y aumentar el rendimiento sin perder datos en el caso de que el formato de destino no admita objetos OLE.

El valor predeterminado es`FALSO`.

### Ejemplos

Muestra cómo ignorar datos OLE durante la carga.

```csharp
// Ignorar los datos OLE puede reducir el consumo de memoria y aumentar el rendimiento
// sin pérdida de datos en caso de que el formato de destino no admita objetos OLE.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


