---
title: TxtSaveOptionsBase.Encoding
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptionsBase propiedad. Especifica la codificación que se utilizará al exportar en formatos de texto. El valor predeterminado es Codificación.UTF8 .
type: docs
weight: 10
url: /es/net/aspose.words.saving/txtsaveoptionsbase/encoding/
---
## TxtSaveOptionsBase.Encoding property

Especifica la codificación que se utilizará al exportar en formatos de texto. El valor predeterminado es **Codificación.UTF8** .

```csharp
public Encoding Encoding { get; set; }
```

### Ejemplos

Muestra cómo configurar la codificación para un documento de salida .txt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregue texto con caracteres fuera del conjunto de caracteres ASCII.
builder.Write("À È Ì Ò Ù.");

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento.
// para modificar cómo guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Verificamos que la propiedad "Codificación" contenga la codificación adecuada para el contenido de nuestro documento.
Assert.AreEqual(System.Text.Encoding.UTF8, txtSaveOptions.Encoding);

doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt", txtSaveOptions);

string docText = System.Text.Encoding.UTF8.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.UTF8.txt"));

Assert.AreEqual("\uFEFFÀ È Ì Ò Ù.\r\n", docText);

// El uso de una codificación inadecuada puede provocar la pérdida del contenido del documento.
txtSaveOptions.Encoding = System.Text.Encoding.ASCII;
doc.Save(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt", txtSaveOptions);
docText = System.Text.Encoding.ASCII.GetString(File.ReadAllBytes(ArtifactsDir + "TxtSaveOptions.Encoding.ASCII.txt"));

Assert.AreEqual("? ? ? ? ?.\r\n", docText);
```

### Ver también

* class [TxtSaveOptionsBase](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* asamblea [Aspose.Words](../../../)


