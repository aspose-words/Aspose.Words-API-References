---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words para .NET
description: Personaliza la propiedad DisplayText de tu FieldGoToButton para mejorar la experiencia del usuario. Configura fácilmente el texto del botón para una navegación fluida y un acceso rápido al documento.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Obtiene o establece el texto del "botón" que aparece en el documento, de forma que pueda seleccionarse para activar el salto.

```csharp
public string DisplayText { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo GOTOBUTTON.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregar un campo GOTOBUTTON. Al hacer doble clic en este campo en Microsoft Word,
// llevará el cursor de texto al marcador cuyo nombre hace referencia la propiedad Ubicación.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Inserte un marcador válido para el campo a referenciar.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Ver también

* class [FieldGoToButton](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
