---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words per .NET
description: Scopri ComHelper, il potente costruttore che inizializza senza sforzo nuove istanze di classe, migliorando l'efficienza e la produttività della tua programmazione.
type: docs
weight: 10
url: /it/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Inizializza una nuova istanza di questa classe.

```csharp
public ComHelper()
```

## Esempi

Mostra come aprire i documenti utilizzando la classe ComHelper.

```csharp
// La classe ComHelper consente di caricare documenti dall'interno dei client COM.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
