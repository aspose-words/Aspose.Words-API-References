---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words para .NET
description: Aspose.Words.Fields.Field clase. Representa un campo de documento de Microsoft Word en C#.
type: docs
weight: 1510
url: /es/net/aspose.words.fields/field/
---
## Field class

Representa un campo de documento de Microsoft Word.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class Field
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe volver a calcular su resultado). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado del campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/#update)() | Realiza la actualización del campo. Se produce si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Realiza una actualización de campo. Se produce si el campo ya se está actualizando. |

## Observaciones

Un campo en un documento de Word es una estructura compleja que consta de múltiples nodos que incluyen el inicio del campo, el código de campo , el separador de campo, el resultado del campo y el final del campo. Los campos pueden estar anidados, contener contenido enriquecido y abarcar varios párrafos o secciones en un documento. El`Field` La clase es un objeto "fachada" que proporciona propiedades y métodos que permiten trabajar con un campo como un solo objeto.

El[`Start`](./start/) ,[`Separator`](./separator/) y[`End`](./end/) Las propiedades apuntan a los nodos de inicio, separador y final del campo respectivamente.

El contenido entre el inicio del campo y el separador es el código de campo. El contenido entre el separador de campo y el final del campo es el resultado del campo. El código de campo normalmente consta de uno o más [`Run`](../../aspose.words/run/) Objetos que especifican instrucciones. Se espera que la aplicación de procesamiento ejecute el código de campo para calcular el resultado del campo.

El proceso de calcular los resultados del campo se llama actualización del campo. Aspose.Words puede actualizar los resultados field de la mayoría de los tipos de campos exactamente de la misma manera que lo hace Microsoft Word. En particular, Aspose.Words puede calcular resultados incluso de los campos de fórmula más complejos. Para calcular el resultado field de un solo campo, utilice el[`Update`](./update/) método. Para actualizar campos en todo el documento use[`UpdateFields`](../../aspose.words/document/updatefields/).

Puede obtener la versión en texto plano del código de campo utilizando el[`GetFieldCode`](./getfieldcode/) método. Puede obtener y configurar la versión de texto sin formato del resultado del campo utilizando el[`Result`](./result/) property. Tanto el código de campo como el resultado del campo pueden contener contenido complejo, como campos anidados, párrafos, formas, tablas y en este caso es posible que desee trabajar con los nodos de campo directamente si necesita más control.

No creas instancias de la`Field` clase directamente. Para crear un nuevo campo utilice el[`InsertField`](../../aspose.words/documentbuilder/insertfield/) método.

## Ejemplos

Muestra cómo insertar un campo en un documento usando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
