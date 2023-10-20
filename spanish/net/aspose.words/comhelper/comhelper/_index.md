---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words para .NET
description: ComHelper constructor. Inicializa una nueva instancia de esta clase en C#.
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

* class [ComHelper](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
