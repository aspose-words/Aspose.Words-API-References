---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words para .NET
description: Descubra el método PclSaveOptions AddPrinterFont para cargar y administrar de manera eficiente las fuentes de impresora de los fabricantes para un mejor rendimiento de impresión.
type: docs
weight: 50
url: /es/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Agrega información sobre la fuente que el fabricante carga en la impresora.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fontFullName | String | Nombre completo de la fuente (por ejemplo, "Times New Roman Bold Italic"). |
| fontPclName | String | Nombre de la fuente que se utiliza en el documento Pcl. |

## Observaciones

Hay 52 fuentes que se deben crear en cualquier impresora según la especificación Pcl. Sin embargo, los fabricantes pueden agregar otras fuentes a sus dispositivos.

## Ejemplos

Muestra cómo hacer que una impresora sustituya todas las instancias de una fuente específica con una fuente diferente.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// Al imprimir este documento, la impresora utilizará la fuente "Courier New"
// para acceder a los lugares donde nuestro documento utilizó la fuente "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Ver también

* class [PclSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
