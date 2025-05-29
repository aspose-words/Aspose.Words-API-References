---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words para .NET
description: Mejore la salida de sus documentos con la propiedad OptimizeOutput de FixedPageSaveOptions. Elimine redundancias y mejore el formato para una visualización más clara.
type: docs
weight: 50
url: /es/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

El indicador indica si es necesario optimizar la salida. Si se establece este indicador, se eliminan los lienzos anidados redundantes y los lienzos vacíos, también se concatenan los glifos vecinos con el mismo formato. Nota: La precisión de la visualización del contenido puede verse afectada si esta propiedad se establece en`verdadero` . El valor predeterminado es`FALSO` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Ejemplos

Muestra cómo optimizar los objetos del documento al guardarlos en XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Crea un objeto "XpsSaveOptions" para pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Establezca la propiedad "OptimizeOutput" en "verdadero" para tomar medidas como eliminar lienzos anidados o vacíos
// y concatenar ejecuciones adyacentes con formato idéntico para optimizar el contenido del documento de salida.
// Esto puede afectar la apariencia del documento.
// Establezca la propiedad "OptimizeOutput" en "falso" para guardar el documento normalmente.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Ver también

* class [FixedPageSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
