---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words para .NET
description: Descubra ComHelper, el poderoso constructor que inicializa sin esfuerzo nuevas instancias de clase, mejorando su eficiencia y productividad de programación.
type: docs
weight: 10
url: /es/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Inicializa una nueva instancia de esta clase.

```csharp
public ComHelper()
```

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

* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
