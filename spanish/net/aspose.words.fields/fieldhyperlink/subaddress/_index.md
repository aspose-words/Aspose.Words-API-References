---
title: FieldHyperlink.SubAddress
linktitle: SubAddress
articleTitle: SubAddress
second_title: Aspose.Words para .NET
description: Descubra la propiedad Subdirección FieldHyperlink para establecer o recuperar fácilmente ubicaciones de archivos o marcadores específicos para una navegación fluida por hipervínculos.
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldhyperlink/subaddress/
---
## FieldHyperlink.SubAddress property

Obtiene o establece una ubicación en el archivo, como un marcador, donde salta este hipervínculo.

```csharp
public string SubAddress { get; set; }
```

## Ejemplos

Muestra cómo utilizar los campos HIPERVÍNCULO para vincular a documentos en el sistema de archivos local.

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
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
