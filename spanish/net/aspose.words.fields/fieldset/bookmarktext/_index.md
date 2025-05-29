---
title: FieldSet.BookmarkText
linktitle: BookmarkText
articleTitle: BookmarkText
second_title: Aspose.Words para .NET
description: Descubra cómo administrar fácilmente la propiedad FieldSet BookmarkText para personalizar y mejorar sus marcadores para una mejor organización y accesibilidad.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldset/bookmarktext/
---
## FieldSet.BookmarkText property

Obtiene o establece el nuevo texto del marcador.

```csharp
public string BookmarkText { get; set; }
```

## Ejemplos

Muestra cómo crear texto marcado con un campo SET y luego mostrarlo en el documento utilizando un campo REF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

 // Nombra el texto marcado con un campo SET.
// Este campo se refiere al "marcador", no a una estructura de marcador que aparece dentro del texto, sino a una variable con nombre.
FieldSet fieldSet = (FieldSet)builder.InsertField(FieldType.FieldSet, false);
fieldSet.BookmarkName = "MyBookmark";
fieldSet.BookmarkText = "Hello world!";
fieldSet.Update();

Assert.AreEqual(" SET  MyBookmark \"Hello world!\"", fieldSet.GetFieldCode());

// Hacer referencia al marcador por nombre en un campo REF y mostrar su contenido.
FieldRef fieldRef = (FieldRef)builder.InsertField(FieldType.FieldRef, true);
fieldRef.BookmarkName = "MyBookmark";
fieldRef.Update();

Assert.AreEqual(" REF  MyBookmark", fieldRef.GetFieldCode());
Assert.AreEqual("Hello world!", fieldRef.Result);

doc.Save(ArtifactsDir + "Field.SET.REF.docx");
```

### Ver también

* class [FieldSet](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
