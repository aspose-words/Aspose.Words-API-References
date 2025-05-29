---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words para .NET
description: Optimice la lectura de documentos con la propiedad TempFolder de LoadOptions. Administre fácilmente los archivos temporales para un procesamiento eficiente y un rendimiento mejorado.
type: docs
weight: 150
url: /es/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Permite utilizar archivos temporales al leer el documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales.

```csharp
public string TempFolder { get; set; }
```

## Observaciones

La carpeta debe existir y ser escribible, de lo contrario se lanzará una excepción.

Aspose.Words elimina automáticamente todos los archivos temporales cuando se completa la lectura.

## Ejemplos

Muestra cómo cargar un documento utilizando archivos temporales.

```csharp
// Tenga en cuenta que este enfoque puede reducir el uso de memoria, pero degrada la velocidad.
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Asegúrese de que el directorio exista y cárguelo
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Muestra cómo utilizar el disco duro en lugar de la memoria al cargar un documento.

```csharp
// Cuando cargamos un documento, varios elementos se almacenan temporalmente en la memoria mientras se produce la operación de guardado.
//Podemos usar esta opción para utilizar una carpeta temporal en el sistema de archivos local en su lugar,
// lo que reducirá la sobrecarga de memoria de nuestra aplicación.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// La carpeta temporal especificada debe existir en el sistema de archivos local antes de la operación de carga.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

//La carpeta persistirá sin contenido residual de la operación de carga.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
