---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: Aspose.Words para .NET
description: Descubra el método DocumentBuilder PopFont para restaurar sin esfuerzo el formato de caracteres desde la pila, mejorando su proceso de creación de documentos.
type: docs
weight: 630
url: /es/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

Recupera el formato de carácter previamente guardado en la pila.

```csharp
public void PopFont()
```

## Ejemplos

Muestra cómo utilizar la pila de formato de un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Configure el formato de fuente y luego escriba el texto que va antes del hipervínculo.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Conservamos nuestra configuración de formato actual en la pila.
builder.PushFont();

// Modifique el formato actual del constructor aplicando un nuevo estilo.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", falso);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Restaura el formato de fuente que guardamos anteriormente y elimina el elemento de la pila.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Ver también

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
