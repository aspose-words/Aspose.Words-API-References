---
title: ComHelper.Open
second_title: Referencia de API de Aspose.Words para .NET
description: ComHelper método. Permite que una aplicación COM cargue unDocument de un archivo.
type: docs
weight: 20
url: /es/net/aspose.words/comhelper/open/
---
## Open(string) {#open_1}

Permite que una aplicación COM cargue un[`Document`](../../document/) de un archivo.

```csharp
public Document Open(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre de archivo del documento a cargar. |

### Valor_devuelto

A[`Document`](../../document/) objeto que representa un documento de Word.

### Observaciones

Este método es igual que llamar al[`Document`](../../document/) constructor con un parámetro de nombre de archivo.

### Ejemplos

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Muestra cómo abrir documentos utilizando la clase ComHelper.

```csharp
// La clase ComHelper nos permite cargar documentos desde clientes COM.
ComHelper comHelper = new ComHelper();

// 1 - Usando un nombre de archivo del sistema local:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - De un flujo:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ver también

* class [Document](../../document/)
* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../comhelper/)
* asamblea [Aspose.Words](../../../)

---

## Open(Stream) {#open}

Permite cargar una aplicación COM[`Document`](../../document/) de un arroyo.

```csharp
public Document Open(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Un objeto de flujo de .NET que contiene el documento que se va a cargar. |

### Valor_devuelto

A[`Document`](../../document/) objeto que representa un documento de Word.

### Observaciones

Este método es igual que llamar al[`Document`](../../document/) constructor con un parámetro de flujo.

### Ejemplos

Muestra cómo abrir documentos utilizando la clase ComHelper.

```csharp
// La clase ComHelper nos permite cargar documentos desde clientes COM.
ComHelper comHelper = new ComHelper();

// 1 - Usando un nombre de archivo del sistema local:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - De un flujo:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ver también

* class [Document](../../document/)
* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../comhelper/)
* asamblea [Aspose.Words](../../../)


