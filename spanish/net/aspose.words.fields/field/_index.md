---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Fields.Field, su clave para mejorar los documentos de Microsoft Word con campos dinámicos para mejorar la funcionalidad y la eficiencia.
type: docs
weight: 1920
url: /es/net/aspose.words.fields/field/
---
## Field class

Representa un campo de documento de Microsoft Word.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class Field
```

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado de campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | Devuelve el texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya se ha eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/#update)() | Realiza la actualización del campo. Se lanza una excepción si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | Realiza una actualización de campo. Se lanza una excepción si el campo ya se está actualizando. |

## Observaciones

Un campo en un documento de Word es una estructura compleja que consta de varios nodos que incluyen el inicio, el código, el separador, el resultado y el final del campo. Los campos pueden estar anidados, contener contenido enriquecido y abarcar varios párrafos o secciones de un documento.`Field` La clase es un objeto "fachada" que proporciona propiedades y métodos que permiten trabajar con un campo como un solo objeto.

El[`Start`](./start/) ,[`Separator`](./separator/) y[`End`](./end/) Las propiedades apuntan a los nodos de inicio, separador y final del campo respectivamente.

El contenido entre el inicio y el separador de campo es el código de campo. El contenido entre el separador de campo y el final del campo es el resultado del campo. El código de campo suele constar de uno o más .[`Run`](../../aspose.words/run/) Objetos que especifican instrucciones. Se espera que la aplicación de procesamiento ejecute el código de campo para calcular el resultado del campo.

El proceso de calcular los resultados de un campo se denomina actualización de campo. Aspose.Words puede actualizar los resultados de field de la mayoría de los tipos de campo de la misma manera que Microsoft Word. Cabe destacar que Aspose.Words puede calcular los resultados incluso de los campos de fórmula más complejos. Para calcular el resultado field de un solo campo, utilice el[`Update`](./update/) Método. Para actualizar los campos de todo el documento utilice[`UpdateFields`](../../aspose.words/document/updatefields/).

Puede obtener la versión de texto simple del código de campo utilizando el[`GetFieldCode`](./getfieldcode/)método. Puede obtener y configurar la versión de texto sin formato del resultado del campo utilizando el método[`Result`](./result/) propiedad. Tanto el código de campo como el resultado del campo pueden contener contenido complejo, como campos anidados, párrafos, formas, tablas y, en este caso, es posible que desee trabajar con los nodos de campo directamente si necesita más control.

No creas instancias del`Field` clase directamente. Para crear un nuevo campo utilice el[`InsertField`](../../aspose.words/documentbuilder/insertfield/) método.

## Ejemplos

Muestra cómo insertar un campo en un documento utilizando un código de campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Esta sobrecarga del método InsertField actualiza automáticamente los campos insertados.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### Ver también

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
