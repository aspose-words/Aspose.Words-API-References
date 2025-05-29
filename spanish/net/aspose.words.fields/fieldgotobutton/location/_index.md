---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words para .NET
description: Descubra la propiedad Ubicación de FieldGoToButton, configure fácilmente marcadores, números de página o elementos para una navegación fluida y una experiencia de usuario mejorada.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Obtiene o establece el nombre de un marcador, un número de página o algún otro elemento al que saltar.

```csharp
public string Location { get; set; }
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
