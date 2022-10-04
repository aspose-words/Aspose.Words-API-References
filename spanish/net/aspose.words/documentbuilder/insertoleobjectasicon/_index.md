---
title: InsertOleObjectAsIcon
second_title: Referencia de API de Aspose.Words para .NET
description: Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE utilizando la extensión de archivo.
type: docs
weight: 380
url: /es/net/aspose.words/documentbuilder/insertoleobjectasicon/
---
## InsertOleObjectAsIcon(string, bool, string, string) {#insertoleobjectasicon_1}

Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE utilizando la extensión de archivo.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Ruta completa al archivo. |
| isLinked | Boolean | Si es verdadero, se inserta el objeto OLE vinculado; de lo contrario, se inserta el objeto OLE incrustado. |
| iconFile | String | Ruta completa al archivo ICO. Si el valor es nulo, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | String | Título del icono. Si el valor es nulo, Aspose.Words utilizará el nombre de archivo. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Generador.

### Ejemplos

Muestra cómo insertar un objeto OLE en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los objetos OLE son enlaces a archivos en nuestro sistema de archivos local que otras aplicaciones instaladas pueden abrir.
// Al hacer doble clic en estas formas, se iniciará la aplicación y luego se usará para abrir el objeto vinculado.
// Hay tres formas de usar el método InsertOleObject para insertar estas formas y configurar su apariencia.
// 1 - Imagen tomada del sistema de archivos local:
using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
{
    // Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
    // el ícono de acuerdo con la extensión del archivo y usa el nombre del archivo para el título del ícono.
    builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", false, false, imageStream); 
}

// Si se omite 'presentación' y se establece 'asIcon', este método sobrecargado selecciona
// el ícono de acuerdo con 'progId' y usa el nombre de archivo para el título del ícono.
// 2 - Icono basado en la aplicación que abrirá el objeto:
builder.InsertOleObject(MyDir + "Spreadsheet.xlsx", "Excel.Sheet", false, true, null);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el icono de acuerdo con 'progId' y utiliza el título de icono predefinido.
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

## InsertOleObjectAsIcon(string, string, bool, string, string) {#insertoleobjectasicon_2}

Inserta un objeto OLE incrustado o vinculado como icono en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE usando el parámetro progID dado.

```csharp
public Shape InsertOleObjectAsIcon(string fileName, string progId, bool isLinked, string iconFile, 
    string iconCaption)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Ruta completa al archivo. |
| progId | String | ProgId del objeto OLE. |
| isLinked | Boolean | Si es verdadero, se inserta el objeto OLE vinculado; de lo contrario, se inserta el objeto OLE incrustado. |
| iconFile | String | Ruta completa al archivo ICO. Si el valor es nulo, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | String | Título del icono. Si el valor es nulo, Aspose.Words utilizará el nombre de archivo. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Generador.

### Ejemplos

Muestra cómo insertar un objeto OLE incrustado o vinculado como icono en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono de acuerdo con 'progId' y usa el nombre de archivo para el título del ícono.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
    // el ícono de acuerdo con la extensión del archivo y usa el nombre del archivo para el título del ícono.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

---

## InsertOleObjectAsIcon(Stream, string, string, string) {#insertoleobjectasicon}

Inserta un objeto OLE incrustado como icono de una secuencia en el documento. Permite especificar el archivo de icono y el título. Detecta el tipo de objeto OLE usando el parámetro progID dado.

```csharp
public Shape InsertOleObjectAsIcon(Stream stream, string progId, string iconFile, 
    string iconCaption)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Secuencia que contiene datos de la aplicación. |
| progId | String | ProgId del objeto OLE. |
| iconFile | String | Ruta completa al archivo ICO. Si el valor es nulo, Aspose.Words utilizará una imagen predefinida. |
| iconCaption | String | Título del icono. Si el valor es nulo, Aspose.Words utilizará el título de un icono predefinido. |

### Valor_devuelto

Nodo de forma que contiene el objeto Ole e insertado en la posición actual del Generador.

### Ejemplos

Muestra cómo insertar un objeto OLE incrustado o vinculado como icono en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
// el ícono de acuerdo con 'progId' y usa el nombre de archivo para el título del ícono.
builder.InsertOleObjectAsIcon(MyDir + "Presentation.pptx", "Package", false, ImageDir + "Logo icon.ico", "My embedded file");

builder.InsertBreak(BreakType.LineBreak);

using (FileStream stream = new FileStream(MyDir + "Presentation.pptx", FileMode.Open))
{
    // Si se omiten 'iconFile' y 'iconCaption', este método sobrecargado selecciona
    // el ícono de acuerdo con la extensión del archivo y usa el nombre del archivo para el título del ícono.
    Shape shape = builder.InsertOleObjectAsIcon(stream, "PowerPoint.Application", ImageDir + "Logo icon.ico",
        "My embedded file stream");

    OlePackage setOlePackage = shape.OleFormat.OlePackage;
    setOlePackage.FileName = "Presentation.pptx";
    setOlePackage.DisplayName = "Presentation.pptx";
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertOleObjectAsIcon.docx");
```

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
