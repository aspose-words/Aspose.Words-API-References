---
title: Class FieldSaveDate
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldSaveDate clase. Implementa el campo SAVEDATE.
type: docs
weight: 2200
url: /es/net/aspose.words.fields/fieldsavedate/
---
## FieldSaveDate class

Implementa el campo SAVEDATE.

```csharp
public class FieldSaveDate : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldSaveDate](fieldsavedate/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [UseLunarCalendar](../../aspose.words.fields/fieldsavedate/uselunarcalendar/) { get; set; } | Obtiene o establece si se usa el calendario Lunar Hijri o el calendario Lunar Hebreo. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldsavedate/usesakaeracalendar/) { get; set; } | Obtiene o establece si usar el calendario Saka Era. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldsavedate/useumalquracalendar/) { get; set; } | Obtiene o establece si usar el calendario Um-al-Qura. |

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

Recupera la fecha y hora en que se guardó el documento por última vez. Por defecto se utiliza el calendario gregoriano.

### Ejemplos

Muestra cómo utilizar el campo SAVEDATE para mostrar la fecha/hora de la operación de guardado más reciente del documento realizada con Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Podemos usar el campo SAVEDATE para mostrar la fecha y hora de la última operación de guardado en el documento.
// La operación de guardado a la que se refieren estos campos es el guardado manual en una aplicación como Microsoft Word,
// no es el método Guardar del documento.
// A continuación se muestran tres tipos de calendario diferentes según los cuales el campo SAVEDATE puede mostrar la fecha/hora.
// 1 - Calendario Lunar Islámico:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Calendario Umm al-Qura:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Calendario nacional indio:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// Los campos SAVEDATE extraen sus valores de fecha/hora de la propiedad integrada LastSavedTime.
// El método Guardar del documento no actualizará este valor, pero aún podemos actualizarlo manualmente.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


