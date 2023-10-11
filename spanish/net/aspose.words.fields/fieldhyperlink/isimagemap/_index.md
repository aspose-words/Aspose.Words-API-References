---
title: FieldHyperlink.IsImageMap
second_title: Referencia de API de Aspose.Words para .NET
description: FieldHyperlink propiedad. Obtiene o establece si se deben agregar coordenadas al hipervínculo para un mapa de imagen del lado del servidor.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Obtiene o establece si se deben agregar coordenadas al hipervínculo para un mapa de imagen del lado del servidor.

```csharp
public bool IsImageMap { get; set; }
```

### Ejemplos

Muestra cómo utilizar los campos HIPERVÍNCULO para vincular documentos en el sistema de archivos local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Cuando hacemos clic en este campo HIPERVÍNCULO en Microsoft Word,
// abrirá el documento vinculado y luego colocará el cursor en el marcador especificado.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Cuando hacemos clic en este campo HIPERVÍNCULO en Microsoft Word,
// abrirá el documento vinculado y se desplazará automáticamente hacia abajo hasta el iframe especificado.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Ver también

* class [FieldHyperlink](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldhyperlink/)
* asamblea [Aspose.Words](../../../)


