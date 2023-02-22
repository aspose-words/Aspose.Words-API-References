---
title: ComHelper.ComHelper
second_title: Aspose.Words per .NET API Reference
description: ComHelper costruttore. Inizializza una nuova istanza di questa classe.
type: docs
weight: 10
url: /it/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Inizializza una nuova istanza di questa classe.

```csharp
public ComHelper()
```

### Esempi

Mostra come aprire documenti utilizzando la classe ComHelper.

```csharp
// La classe ComHelper ci consente di caricare documenti dai client COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilizzo di un nome file di sistema locale:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Da un flusso:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Guarda anche

* class [ComHelper](../)
* spazio dei nomi [Aspose.Words](../../comhelper/)
* assemblea [Aspose.Words](../../../)


