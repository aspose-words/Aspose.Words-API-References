---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParagraphFormat Bidi para controlar fácilmente el formato de texto de derecha a izquierda para mejorar la legibilidad y el diseño del documento.
type: docs
weight: 50
url: /es/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Obtiene o establece si este es un párrafo de derecha a izquierda.

```csharp
public bool Bidi { get; set; }
```

## Observaciones

Cuando`verdadero`, las carreras y otros objetos en línea en este párrafo se disponen de derecha a izquierda.

## Ejemplos

Muestra cómo detectar la dirección del texto de un documento de texto sin formato.

```csharp
// Crea un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
// para modificar la forma en que cargamos un documento de texto plano.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Establezca la propiedad "DocumentDirection" en "DocumentDirection.Auto" detecta automáticamente
// la dirección de cada párrafo de texto que Aspose.Words carga desde texto simple.
//La propiedad "Bidi" de cada párrafo almacenará su dirección.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Detecta texto hebreo de derecha a izquierda.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Detecta texto en inglés de derecha a izquierda.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

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

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
