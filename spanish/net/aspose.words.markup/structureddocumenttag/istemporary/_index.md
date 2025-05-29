---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad StructuredDocumentTag IsTemporary determina si su SDT se elimina de WordProcessingML al cambiar el contenido. ¡Optimice sus documentos hoy mismo!
type: docs
weight: 160
url: /es/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

Especifica si esto**TED** se eliminará del documento WordProcessingML cuando se modifique su contenido.

```csharp
public bool IsTemporary { get; set; }
```

## Ejemplos

Muestra cómo realizar controles de un solo uso.

```csharp
Document doc = new Document();

// Insertar una etiqueta de documento estructurado de texto simple,
// que actuará como un formato de texto simple en el que el usuario podrá ingresar texto.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Establezca la propiedad "IsTemporary" en "true" para que la etiqueta del documento estructurado desaparezca y
// asimilar su contenido en el documento después de que el usuario lo edite una vez en Microsoft Word.
// Establezca la propiedad "IsTemporary" en "falso" para permitir que el usuario edite el contenido
// de la etiqueta del documento estructurado cualquier número de veces.
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// Inserte otra etiqueta de documento estructurado en forma de casilla de verificación y establezca su estado predeterminado en "marcado".
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// Establezca la propiedad "IsTemporary" en "verdadero" para que la casilla de verificación se convierta en un símbolo
// una vez que el usuario hace clic en él en Microsoft Word.
// Establezca la propiedad "IsTemporary" en "falso" para permitir que el usuario haga clic en la casilla de verificación cualquier cantidad de veces.
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### Ver también

* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
