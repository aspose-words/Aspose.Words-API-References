---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Restaura tu texto a su estilo original con el método Font ClearFormatting. ¡Disfruta de un formato limpio y consistente para una apariencia impecable!
type: docs
weight: 560
url: /es/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Restablece el formato de fuente predeterminado.

```csharp
public void ClearFormatting()
```

## Observaciones

Elimina todo el formato de fuente especificado explícitamente en el objeto del cual [`Font`](../) Se obtuvo para que el formato de fuente se herede de el padre apropiado.

## Ejemplos

Muestra cómo insertar un campo de hipervínculo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserta un hipervínculo y enfatízalo con formato personalizado.
// El hipervínculo será un fragmento de texto en el que se puede hacer clic y que nos llevará a la ubicación especificada en la URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falso);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic izquierdo en el enlace del texto en Microsoft Word nos llevará a la URL a través de una nueva ventana del navegador web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
