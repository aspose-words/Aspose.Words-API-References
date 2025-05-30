---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: Administre el texto de FieldShape fácilmente obtenga o establezca valores sin esfuerzo para una recuperación de datos perfecta y una funcionalidad mejorada en sus aplicaciones.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

Obtiene o establece el texto a recuperar.

```csharp
public string Text { get; set; }
```

## Ejemplos

Muestra cómo crear listas compatibles con idiomas de derecha a izquierda con campos BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// El campo BIDIOUTLINE numera los párrafos como los campos AUTONUM/LISTNUM,
// pero solo es visible cuando está habilitado un idioma de edición de derecha a izquierda, como hebreo o árabe.
// El siguiente campo mostrará ".1", el equivalente RTL de la lista número "1".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Agregue dos campos BIDIOUTLINE más, que mostrarán ".2" y ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Establezca la alineación del texto horizontal para cada párrafo del documento en RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Si habilitamos un idioma de edición de derecha a izquierda en Microsoft Word, nuestros campos mostrarán números.
// De lo contrario, mostrarán "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

Muestra cómo se manejan algunos campos más antiguos de Microsoft Word, como FORMA e INSERTAR, durante la carga.

```csharp
//Abre un documento creado en Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Si abrimos el documento de Word y presionamos Alt+F9, veremos un campo FORMA y un campo INCORPORAR.
// Un campo SHAPE es el ancla/lienzo para un objeto AutoShape con el estilo de ajuste "En línea con el texto" habilitado.
// Un campo EMBED tiene la misma función, pero para un objeto incrustado,
// como una hoja de cálculo de un documento de Excel externo.
// Sin embargo, estos campos no aparecerán en la colección Campos del documento.
Assert.AreEqual(0, doc.Range.Fields.Count);

//Estos campos solo son compatibles con versiones antiguas de Microsoft Word.
// El proceso de carga del documento convertirá estos campos en objetos Shape,
// a la que podemos acceder en la colección de nodos del documento.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// El primer nodo Forma corresponde al campo FORMA en el documento de entrada,
// que es el lienzo en línea para la autoforma.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

//El segundo nodo Forma es la Autoforma en sí.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

//La tercera forma es lo que era el campo EMBED que contenía la hoja de cálculo externa.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Ver también

* class [FieldShape](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
