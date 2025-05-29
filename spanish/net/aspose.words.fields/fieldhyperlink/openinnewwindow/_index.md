---
title: FieldHyperlink.OpenInNewWindow
linktitle: OpenInNewWindow
articleTitle: OpenInNewWindow
second_title: Aspose.Words para .NET
description: Descubra la propiedad FieldHyperlink OpenInNewWindow, controle fácilmente si los enlaces se abren en una nueva ventana del navegador para una mejor experiencia del usuario.
type: docs
weight: 40
url: /es/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

Obtiene o establece si se debe abrir el sitio de destino en una nueva ventana del navegador web.

```csharp
public bool OpenInNewWindow { get; set; }
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
