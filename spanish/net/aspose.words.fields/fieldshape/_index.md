---
title: FieldShape
second_title: Referencia de API de Aspose.Words para .NET
description: Implementa el campo FORMA.
type: docs
weight: 2260
url: /es/net/aspose.words.fields/fieldshape/
---
## FieldShape class

Implementa el campo FORMA.

```csharp
public class FieldShape : Field
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [FieldShape](fieldshape)() | Constructor predeterminado |

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
| [Text](../../aspose.words.fields/fieldshape/text) { get; set; } | Obtiene o establece el texto a recuperar. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Obtiene el tipo de campo de Microsoft Word. |

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

Recupera el texto especificado.

### Ejemplos

Muestra cómo crear listas compatibles con el idioma de derecha a izquierda con campos BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// El campo BIDIOUTLINE numera párrafos como los campos AUTONUM/LISTNUM,
// pero solo es visible cuando está habilitado un idioma de edición de derecha a izquierda, como el hebreo o el árabe.
// El siguiente campo mostrará ".1", el equivalente RTL del número de lista "1".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Agregue dos campos BIDIOUTLINE más, que mostrarán ".2" y ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Establecer la alineación de texto horizontal para cada párrafo del documento en RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Si habilitamos un idioma de edición de derecha a izquierda en Microsoft Word, nuestros campos mostrarán números.
// De lo contrario, mostrarán "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Muestra cómo se manejan algunos campos antiguos de Microsoft Word, como SHAPE e EMBED, durante la carga.

```csharp
// Abra un documento que se creó en Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Si abrimos el documento de Word y presionamos Alt+F9, veremos un campo FORMA y un campo EMBED.
// Un campo FORMA es el ancla/lienzo para un objeto AutoForma con el estilo de ajuste "En línea con el texto" habilitado.
// Un campo EMBED tiene la misma función, pero para un objeto incrustado,
// como una hoja de cálculo de un documento de Excel externo.
// Sin embargo, estos campos no aparecerán en la colección Fields del documento.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Estos campos solo son compatibles con versiones anteriores de Microsoft Word.
// El proceso de carga del documento convertirá estos campos en objetos Shape,
// al que podemos acceder en la colección de nodos del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// El primer nodo Forma corresponde al campo FORMA en el documento de entrada,
// que es el lienzo en línea para la autoforma.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// El segundo nodo Forma es la autoforma misma.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// La tercera Forma es lo que era el campo EMBED que contenía la hoja de cálculo externa.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ver también

* class [Field](../field)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
