---
title: FieldDate
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo FECHA.
type: docs
weight: 1620
url: /es/net/aspose.words.fields/fielddate/
---
## FieldDate class

Implementa el campo FECHA.

```csharp
public class FieldDate : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldDate](fielddate)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Obtiene un[`FieldFormat`](../fieldformat) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe recalcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser nulo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |
| [UseLastFormat](../../aspose.words.fields/fielddate/uselastformat) { get; set; } | Obtiene o establece si se debe utilizar un formato utilizado por última vez por la aplicación de hospedaje al insertar un nuevo campo de FECHA. |
| [UseLunarCalendar](../../aspose.words.fields/fielddate/uselunarcalendar) { get; set; } | Obtiene o establece si se usa el calendario Lunar Hijri o el calendario Lunar Hebreo. |
| [UseSakaEraCalendar](../../aspose.words.fields/fielddate/usesakaeracalendar) { get; set; } | Obtiene o establece si usar el calendario Saka Era. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fielddate/useumalquracalendar) { get; set; } | Obtiene o establece si usar el calendario Um-al-Qura. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve **nulo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Realiza el desvinculado del campo. |
| [Update](../../aspose.words.fields/field/update)() | Realiza la actualización del campo. Se lanza si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update)(bool) | Realiza una actualización de campo. Se lanza si el campo ya se está actualizando. |

### Observaciones

Inserta la fecha y hora actual. Por defecto se utiliza el calendario gregoriano.

### Ejemplos

Muestra cómo usar los campos de FECHA para mostrar fechas de acuerdo con diferentes tipos de calendarios.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si queremos que el texto del documento muestre siempre la fecha correcta, podemos usar un campo FECHA.
// A continuación se muestran tres tipos de calendarios culturales que un campo FECHA puede usar para mostrar una fecha.
// 1 - Calendario Lunar Islámico:
FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLunarCalendar = true;
Assert.AreEqual(" DATE  \\h", field.GetFieldCode());
builder.Writeln();

// 2 - Calendario Umm al-Qura:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseUmAlQuraCalendar = true;
Assert.AreEqual(" DATE  \\u", field.GetFieldCode());
builder.Writeln();

// 3 - Calendario Nacional Indio:
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseSakaEraCalendar = true;
Assert.AreEqual(" DATE  \\s", field.GetFieldCode());
builder.Writeln();

// Inserte un campo de FECHA y establezca su tipo de calendario en el último utilizado por la aplicación host.
// En Microsoft Word, el tipo será el utilizado más recientemente en Insertar -> Texto -> Cuadro de diálogo Fecha y hora.
field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.UseLastFormat = true;
Assert.AreEqual(" DATE  \\l", field.GetFieldCode());
builder.Writeln();

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.DATE.docx");
```

### Ver también

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
