---
title: Class FieldInclude
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldInclude clase. Implementa el campo INCLUYE.
type: docs
weight: 1880
url: /es/net/aspose.words.fields/fieldinclude/
---
## FieldInclude class

Implementa el campo INCLUYE.

```csharp
public class FieldInclude : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldInclude](fieldinclude/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldinclude/bookmarkname/) { get; set; } | Obtiene o establece el nombre del marcador en el documento a incluir. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [LockFields](../../aspose.words.fields/fieldinclude/lockfields/) { get; set; } | Obtiene o establece si se debe evitar que se actualicen los campos del documento incluido. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [SourceFullName](../../aspose.words.fields/fieldinclude/sourcefullname/) { get; set; } | Obtiene o establece la ubicación del documento. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [TextConverter](../../aspose.words.fields/fieldinclude/textconverter/) { get; set; } | Obtiene o establece el nombre del convertidor de texto para el formato del archivo incluido. |
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

Inserta todo o parte del texto y gráficos contenidos en otro documento.

### Ejemplos

Muestra cómo crear un campo INCLUDE y establecer sus propiedades.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos usar un campo INCLUDE para importar una parte de otro documento en el sistema de archivos local.
// El marcador del otro documento al que hacemos referencia con este campo contiene esta parte importada.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


