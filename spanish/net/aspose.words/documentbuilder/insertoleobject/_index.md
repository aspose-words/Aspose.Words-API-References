---
title: DocumentBuilder.InsertOleObject
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder método. Inserta un objeto OLE incrustado de una secuencia en el documento.
type: docs
weight: 400
url: /es/net/aspose.words/documentbuilder/insertoleobject/
---
## InsertOleObject(Stream, string, bool, Stream) {#insertoleobject}

Inserta un objeto OLE incrustado de una secuencia en el documento.

```csharp
public Shape InsertOleObject(Stream stream, string progId, bool asIcon, Stream presentation)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Flujo que contiene datos de la aplicación. |
| progId | String | Identificador programático del objeto OLE. |
| asIcon | Boolean | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | Stream | Presentación de imagen del objeto OLE. Si el valor es`nulo` Aspose.Words utilizará una de las imágenes predefinidas. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Constructor.

### Ejemplos

Muestra cómo utilizar el generador de documentos para incrustar objetos OLE en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar una hoja de cálculo de Microsoft Excel desde el sistema de archivos local
// en el documento manteniendo su apariencia predeterminada.
using (Stream spreadsheetStream = File.Open(MyDir + "Spreadsheet.xlsx", FileMode.Open))
{
    builder.Writeln("Spreadsheet Ole object:");
    // Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
    // el icono según 'progId' y utiliza el título del icono predefinido.
    builder.InsertOleObject(spreadsheetStream, "OleObject.xlsx", false, null);
}

// Insertar una presentación de Microsoft Powerpoint como un objeto OLE.
// Esta vez, tendrá una imagen descargada de la web como ícono.
using (Stream powerpointStream = File.Open(MyDir + "Presentation.pptx", FileMode.Open))
{
    using (HttpClient httpClient = new HttpClient())
    {
        byte[] imgBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

        using (MemoryStream imageStream = new MemoryStream(imgBytes))
        {
            builder.InsertParagraph();
            builder.Writeln("Powerpoint Ole object:");
            builder.InsertOleObject(powerpointStream, "OleObject.pptx", true, imageStream);
        }
    }
}

// Haga doble clic en estos objetos en Microsoft Word para abrir
// los archivos vinculados usando sus respectivas aplicaciones.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjects.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOleObject(string, bool, bool, Stream) {#insertoleobject_1}

Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE usando la extensión de archivo.

```csharp
public Shape InsertOleObject(string fileName, bool isLinked, bool asIcon, Stream presentation)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Ruta completa al archivo. |
| isLinked | Boolean | Si`verdadero` luego se inserta el objeto OLE vinculado; de lo contrario, se inserta el objeto OLE incrustado. |
| asIcon | Boolean | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | Stream | Presentación de imagen del objeto OLE. Si el valor es`nulo` Aspose.Words utilizará una de las imágenes predefinidas. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Constructor.

### Ejemplos

Muestra cómo insertar un objeto OLE en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los objetos OLE son enlaces a archivos de nuestro sistema de archivos local que otras aplicaciones instaladas pueden abrir.
// Al hacer doble clic en estas formas se iniciará la aplicación y luego se usará para abrir el objeto vinculado.
// Hay tres formas de utilizar el método InsertOleObject para insertar estas formas y configurar su apariencia.
// 1 - Imagen tomada del sistema de archivos local:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
    // el icono según la extensión del archivo y utiliza el nombre del archivo para el título del icono.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
// el icono según 'progId' y utiliza el nombre del archivo para el título del icono.
// 2 - Icono basado en la aplicación que abrirá el objeto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el icono según 'progId' y utiliza el título del icono predefinido.
// 3 - Icono de imagen de 32 x 32 píxeles o menos del sistema de archivos local, con un título personalizado:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOleObject(string, string, bool, bool, Stream) {#insertoleobject_2}

Inserta un objeto OLE incrustado o vinculado desde un archivo en el documento. Detecta el tipo de objeto OLE utilizando el parámetro progID dado.

```csharp
public Shape InsertOleObject(string fileName, string progId, bool isLinked, bool asIcon, 
    Stream presentation)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Ruta completa al archivo. |
| progId | String | ProgId del objeto OLE. |
| isLinked | Boolean | Si`verdadero` luego se inserta el objeto OLE vinculado; de lo contrario, se inserta el objeto OLE incrustado. |
| asIcon | Boolean | Especifica el modo Icónico o Normal del objeto OLE que se inserta. |
| presentation | Stream | Presentación de imagen del objeto OLE. Si el valor es`nulo` Aspose.Words utilizará una de las imágenes predefinidas. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Constructor.

### Ejemplos

Muestra cómo insertar un objeto OLE en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los objetos OLE son enlaces a archivos de nuestro sistema de archivos local que otras aplicaciones instaladas pueden abrir.
// Al hacer doble clic en estas formas se iniciará la aplicación y luego se usará para abrir el objeto vinculado.
// Hay tres formas de utilizar el método InsertOleObject para insertar estas formas y configurar su apariencia.
// 1 - Imagen tomada del sistema de archivos local:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
    // el icono según la extensión del archivo y utiliza el nombre del archivo para el título del icono.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
// el icono según 'progId' y utiliza el nombre del archivo para el título del icono.
// 2 - Icono basado en la aplicación que abrirá el objeto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el icono según 'progId' y utiliza el título del icono predefinido.
// 3 - Icono de imagen de 32 x 32 píxeles o menos del sistema de archivos local, con un título personalizado:
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", false, ImageDir + "Logo icon.ico",
    "Double click to view presentation!");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObject.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


