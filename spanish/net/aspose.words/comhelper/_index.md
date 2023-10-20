---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words para .NET
description: Aspose.Words.ComHelper clase. Proporciona métodos para que los clientes COM carguen un documento en Aspose.Words en C#.
type: docs
weight: 220
url: /es/net/aspose.words/comhelper/
---
## ComHelper class

Proporciona métodos para que los clientes COM carguen un documento en Aspose.Words.

```csharp
public class ComHelper
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ComHelper](comhelper/)() | Inicializa una nueva instancia de esta clase. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Permite cargar una aplicación COM[`Document`](../document/) de una secuencia. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Permite que una aplicación COM cargue un[`Document`](../document/) desde un archivo. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Permite que una aplicación COM cargue un[`Document`](../document/) desde un objeto IStream. |

## Observaciones

Utilizar el`ComHelper` clase para cargar un documento desde un archivo o secuencia en un [`Document`](../document/) objeto en una aplicación COM.

El[`Document`](../document/) La clase proporciona un constructor predeterminado para crear un nuevo documento y también proporciona constructores sobrecargados para cargar un documento desde un archivo o secuencia. Si está utilizando Aspose.Words desde una aplicación .NET, puede utilizar todos los[`Document`](../document/) constructores directamente, pero si está utilizando Aspose.Words desde una aplicación COM, solo el valor predeterminado[`Document`](../document/) constructor está disponible.

## Ejemplos

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Muestra cómo abrir documentos usando la clase ComHelper.

```csharp
// La clase ComHelper nos permite cargar documentos desde clientes COM.
ComHelper comHelper = new ComHelper();

// 1 - Usando un nombre de archivo del sistema local:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Desde una secuencia:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
