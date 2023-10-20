---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words para .NET
description: SaveOptions TempFolder propiedad. Especifica la carpeta para archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada esta propiedad esnulo y no se utilizan archivos temporales en C#.
type: docs
weight: 140
url: /es/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Especifica la carpeta para archivos temporales utilizados al guardar en un archivo DOC o DOCX. De forma predeterminada, esta propiedad es`nulo` y no se utilizan archivos temporales.

```csharp
public string TempFolder { get; set; }
```

## Observaciones

Cuando Aspose.Words guarda un documento, necesita crear estructuras internas temporales. De forma predeterminada, estas estructuras internas se crean en la memoria y el uso de la memoria aumenta durante un breve período mientras se guarda el documento. Cuando se completa el guardado, el recolector de basura libera y recupera la memoria.

Si está guardando un documento muy grande (miles de páginas) y/o procesando muchos documentos al mismo tiempo, entonces el pico de memoria durante el guardado puede ser lo suficientemente significativo como para hacer que el sistema arrojeOutOfMemoryException . Especificando una carpeta temporal usando`TempFolder` Hará que Aspose.Words mantenga las estructuras internas en archivos temporales en lugar de memoria. Reduce el uso de memoria durante el guardado, pero disminuirá el rendimiento del guardado.

La carpeta debe existir y poder escribirse; de lo contrario, se generará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando se completa el guardado.

## Ejemplos

Muestra cómo utilizar el disco duro en lugar de la memoria al guardar un documento.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando guardamos un documento, varios elementos se almacenan temporalmente en la memoria mientras se realiza la operación de guardado.
// Podemos usar esta opción para usar una carpeta temporal en el sistema de archivos local,
// lo que reducirá la sobrecarga de memoria de nuestra aplicación.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de guardar.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// La carpeta persistirá sin contenido residual de la operación de carga.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
