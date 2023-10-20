---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words para .NET
description: FixedPageSaveOptions OptimizeOutput propiedad. El indicador indica si es necesario optimizar la salida. Si este indicador se establece en lienzos anidados redundantes y se eliminan los lienzos vacíos también se concatenan los glifos vecinos con el mismo formato. Nota La precisión de la visualización del contenido puede verse afectada si esta propiedad está establecida enverdadero . El valor predeterminado esFALSO  en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

El indicador indica si es necesario optimizar la salida. Si este indicador se establece en lienzos anidados redundantes y se eliminan los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad está establecida en`verdadero` . El valor predeterminado es`FALSO` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Ejemplos

Muestra cómo optimizar los objetos del documento mientras se guarda en XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Crea un objeto "XpsSaveOptions" para pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// Establece la propiedad "OptimizeOutput" en "true" para tomar medidas como eliminar lienzos anidados o vacíos
// y concatenar ejecuciones adyacentes con formato idéntico para optimizar el contenido del documento de salida.
// Esto puede afectar la apariencia del documento.
// Establece la propiedad "OptimizeOutput" en "false" para guardar el documento normalmente.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Ver también

* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
