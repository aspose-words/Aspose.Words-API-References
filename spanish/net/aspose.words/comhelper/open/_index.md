---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words para .NET
description: Descubra la integración perfecta con el método abierto de ComHelper, lo que permite cargar documentos sin esfuerzo desde archivos para sus aplicaciones COM.
type: docs
weight: 20
url: /es/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Permite que una aplicación COM cargue un[`Document`](../../document/) de un archivo.

```csharp
public Document Open(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | Nombre del archivo del documento a cargar. |

### Valor_devuelto

A[`Document`](../../document/) objeto que representa un documento de Word.

## Observaciones

Este método es el mismo que llamar al[`Document`](../../document/) constructor con un parámetro de nombre de archivo.

## Ejemplos

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Muestra cómo abrir documentos utilizando la clase ComHelper.

```csharp
//La clase ComHelper nos permite cargar documentos desde dentro de los clientes COM.
ComHelper comHelper = new ComHelper();

// 1 - Usando un nombre de archivo del sistema local:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Desde un stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ver también

* class [Document](../../document/)
* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Permite que se cargue una aplicación COM[`Document`](../../document/) de un arroyo.

```csharp
public Document Open(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | Un objeto de flujo .NET que contiene el documento a cargar. |

### Valor_devuelto

A[`Document`](../../document/) objeto que representa un documento de Word.

## Observaciones

Este método es el mismo que llamar al[`Document`](../../document/) constructor con un parámetro de flujo.

## Ejemplos

Muestra cómo abrir documentos utilizando la clase ComHelper.

```csharp
//La clase ComHelper nos permite cargar documentos desde dentro de los clientes COM.
ComHelper comHelper = new ComHelper();

// 1 - Usando un nombre de archivo del sistema local:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Desde un stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ver también

* class [Document](../../document/)
* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
