---
title: FieldGoToButton.DisplayText
second_title: Referencia de API de Aspose.Words para .NET
description: FieldGoToButton propiedad. Obtiene o establece el texto del botón que aparece en el documento de forma que se pueda seleccionar para activar el salto.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Obtiene o establece el texto del "botón" que aparece en el documento, de forma que se pueda seleccionar para activar el salto.

```csharp
public string DisplayText { get; set; }
```

### Ejemplos

Muestra para insertar un campo GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega un campo GOTOBUTTON. Cuando hacemos doble clic en este campo en Microsoft Word,
// llevará el cursor de texto al marcador cuyo nombre hace referencia la propiedad Ubicación.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Inserta un marcador válido para el campo al que se hace referencia.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Ver también

* class [FieldGoToButton](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldgotobutton/)
* asamblea [Aspose.Words](../../../)


