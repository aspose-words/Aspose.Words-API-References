---
title: Class FieldListNum
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Fields.FieldListNum clase. Implementa el campo LISTNUM.
type: docs
weight: 2120
url: /es/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implementa el campo LISTNUM.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) artículo de documentación.

```csharp
public class FieldListNum : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Obtiene el texto que representa el resultado del campo mostrado. |
| [End](../../aspose.words.fields/field/end/) { get; } | Obtiene el nodo que representa el final del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Obtiene un[`FieldFormat`](../fieldformat/) objeto que proporciona acceso escrito al formato del campo. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Devuelve un valor que indica si el código del campo proporciona el nombre de una definición de numeración abstracta . |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Obtiene o establece si el resultado actual del campo ya no es correcto (obsoleto) debido a otras modificaciones realizadas en el documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Obtiene o establece si el campo está bloqueado (no debe volver a calcular su resultado). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Obtiene o establece el nivel en la lista, anulando el comportamiento predeterminado del campo. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Obtiene o establece el nombre de la definición de numeración abstracta utilizada para la numeración. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Obtiene o establece el LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Obtiene o establece el texto que se encuentra entre el separador de campo y el final del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Obtiene el nodo que representa el separador de campos. Puede ser`nulo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Obtiene el nodo que representa el inicio del campo. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Obtiene o establece el valor inicial para este campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Obtiene el tipo de campo de Microsoft Word. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). Se incluyen tanto el código de campo como el resultado del campo de los campos secundarios. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Devuelve texto entre el inicio del campo y el separador de campo (o el final del campo si no hay separador). |
| [Remove](../../aspose.words.fields/field/remove/)() | Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo principal, devuelve su párrafo principal. Si el campo ya está eliminado, devuelve`nulo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Realiza la desvinculación del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Realiza la actualización del campo. Se produce si el campo ya se está actualizando. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Realiza una actualización de campo. Se produce si el campo ya se está actualizando. |

### Ejemplos

Muestra cómo numerar párrafos con campos LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Los campos LISTNUM muestran un número que se incrementa en cada campo LISTNUM.
// Estos campos también tienen una variedad de opciones que nos permiten usarlos para emular listas numeradas.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Las listas comienzan a contar en 1 de forma predeterminada, pero podemos establecer este número en un valor diferente, como 0.
// Este campo mostrará "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // Los campos LISTNUM mantienen recuentos separados para cada nivel de lista.
// Insertar un campo LISTNUM en el mismo párrafo que otro campo LISTNUM
// aumenta el nivel de la lista en lugar del recuento.
// El siguiente campo continuará el recuento que comenzamos anteriormente y mostrará un valor de "1" en el nivel de lista 1.
builder.InsertField(FieldType.FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 2. Mostrará un valor de "1".
builder.InsertField(FieldType.FieldListNum, true);

// Este campo iniciará un recuento en el nivel de lista 3. Mostrará un valor de "1".
// Diferentes niveles de lista tienen diferentes formatos,
// entonces estos campos combinados mostrarán un valor de "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// El siguiente campo LISTNUM que insertemos continuará el recuento a nivel de lista
// que el campo LISTNUM anterior estaba activado.
// Podemos usar la propiedad "ListLevel" para saltar a un nivel de lista diferente.
// Si este campo LISTNUM permaneciera en el nivel de lista 3, mostraría "ii)",
// pero, como lo hemos movido al nivel de lista 2, continúa el conteo en ese nivel y muestra "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Podemos configurar la propiedad ListName para que el campo emule un tipo de campo AUTONUM diferente.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// y "LegalDefault" emula los campos AUTONUMLGL.
// El nombre de la lista "OutlineDefault" con 1 como número inicial dará como resultado que se muestre "I".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName no se transfiere del campo anterior, por lo que tendremos que configurarlo para cada campo nuevo.
// Este campo continúa el recuento con el nombre de la lista diferente y muestra "II".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Ver también

* class [Field](../field/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)


