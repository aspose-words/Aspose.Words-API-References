---
title: FieldLastSavedBy Class
linktitle: FieldLastSavedBy
articleTitle: FieldLastSavedBy
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.FieldLastSavedBy para optimizar la gestión de documentos con la funcionalidad del campo LASTSAVEDBY. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 2510
url: /es/net/aspose.words.fields/fieldlastsavedby/
---
## FieldLastSavedBy class

Implementa el campo LASTSAVEDBY.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class FieldLastSavedBy : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldLastSavedBy](fieldlastsavedby/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/)objeto que proporciona acceso tipificado al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que está entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campo. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Observaciones

Recupera el nombre del usuario que modificó y guardó por última vez el documento actual, tal como está registrado en el**Última modificación por** Propiedad de las propiedades integradas del documento.

## Ejemplos

Muestra cómo utilizar el campo LASTSAVEDBY.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si creamos un documento en Microsoft Word, tendrá el nombre del usuario en la propiedad incorporada "Último guardado por".
 // Si creamos un documento programáticamente, esta propiedad será nula y necesitaremos asignarle un valor.
doc.BuiltInDocumentProperties.LastSavedBy = "John Doe";

//Podemos utilizar el campo LASTSAVEDBY para mostrar el valor de esta propiedad en el documento.
FieldLastSavedBy field = (FieldLastSavedBy)builder.InsertField(FieldType.FieldLastSavedBy, true);

Assert.AreEqual(" LASTSAVEDBY ", field.GetFieldCode());
Assert.AreEqual("John Doe", field.Result);

doc.Save(ArtifactsDir + "Field.LASTSAVEDBY.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
