---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words para .NET
description: Optimice el guardado de sus documentos con la propiedad SaveOptions TempFolder, que designa una carpeta para archivos temporales DOC y DOCX, mejorando la eficiencia.
type: docs
weight: 140
url: /es/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Especifica la carpeta para los archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales.

```csharp
public string TempFolder { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| OutOfMemoryException | Se lanza si está guardando un documento muy grande (miles de páginas) y/o procesando muchos documentos al mismo tiempo. El pico de memoria durante el guardado puede ser lo suficientemente significativo como para provocar la excepción. |

## Observaciones

Cuando Aspose.Words guarda un documento, necesita crear estructuras internas temporales. De forma predeterminada, estas estructuras internas se crean en memoria y el uso de memoria se dispara durante un breve periodo mientras se guarda el documento. Al finalizar el guardado, el recolector de elementos no utilizados libera memoria y la recupera.

Especificar una carpeta temporal usando`TempFolder` Hará que Aspose.Words guarde las estructuras internas en archivos temporales en lugar de en la memoria. Esto reduce el uso de memoria al guardar, pero disminuye el rendimiento.

La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando se completa el guardado.

## Ejemplos

Muestra cómo utilizar el disco duro en lugar de la memoria al guardar un documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando guardamos un documento, varios elementos se almacenan temporalmente en la memoria mientras se realiza la operación de guardado.
//Podemos usar esta opción para utilizar una carpeta temporal en el sistema de archivos local en su lugar,
// lo que reducirá la sobrecarga de memoria de nuestra aplicación.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de guardado.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

//La carpeta persistirá sin contenido residual de la operación de carga.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
