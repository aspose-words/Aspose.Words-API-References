---
title: FieldIncludePicture
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo INCLUDEPICTURE.
type: docs
weight: 1890
url: /es/net/aspose.words.fields/fieldincludepicture/
---
## FieldIncludePicture class

Implementa el campo INCLUDEPICTURE.

```csharp
public class FieldIncludePicture : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldIncludePicture](fieldincludepicture/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [GraphicFilter](../../aspose.words.fields/fieldincludepicture/graphicfilter/) { get; set; } | Obtiene o establece el nombre del filtro para el formato del gráfico a insertar. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLinked](../../aspose.words.fields/fieldincludepicture/islinked/) { get; set; } | Obtiene o establece si se reduce el tamaño del archivo al no almacenar datos gráficos con el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [ResizeHorizontally](../../aspose.words.fields/fieldincludepicture/resizehorizontally/) { get; set; } | Obtiene o establece si cambiar el tamaño de la imagen horizontalmente desde la fuente. |
| [ResizeVertically](../../aspose.words.fields/fieldincludepicture/resizevertically/) { get; set; } | Obtiene o establece si cambiar el tamaño de la imagen verticalmente desde la fuente. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SourceFullName](../../aspose.words.fields/fieldincludepicture/sourcefullname/) { get; set; } | Obtiene o establece la ubicación de la imagen usando un IRI. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Recupera una imagen y la muestra como resultado del campo.

### Ejemplos

Muestra cómo insertar imágenes usando los campos IMPORT e INCLUDEPICTURE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación hay dos tipos de campos similares que podemos usar para mostrar imágenes vinculadas desde el sistema de archivos local.
// 1 - El campo INCLUYE IMAGEN:
FieldIncludePicture fieldIncludePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
fieldIncludePicture.SourceFullName = ImageDir + "Transparent background logo.png";

Assert.True(Regex.Match(fieldIncludePicture.GetFieldCode(), " INCLUDEPICTURE  .*").Success);

// Aplicar el filtro PNG32.FLT.
fieldIncludePicture.GraphicFilter = "PNG32";
fieldIncludePicture.IsLinked = true;
fieldIncludePicture.ResizeHorizontally = true;
fieldIncludePicture.ResizeVertically = true;

// 2 - El campo IMPORTAR:
FieldImport fieldImport = (FieldImport)builder.InsertField(FieldType.FieldImport, true);
fieldImport.SourceFullName = ImageDir + "Transparent background logo.png";
fieldImport.GraphicFilter = "PNG32";
fieldImport.IsLinked = true;

Assert.True(Regex.Match(fieldImport.GetFieldCode(), " IMPORT  .* \\\\c PNG32 \\\\d").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IMPORT.INCLUDEPICTURE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
