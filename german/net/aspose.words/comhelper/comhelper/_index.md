---
title: ComHelper.ComHelper
second_title: Aspose.Words für .NET-API-Referenz
description: ComHelper constructeur. Initialisiert eine neue Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public ComHelper()
```

### Beispiele

Zeigt, wie Dokumente mit der ComHelper-Klasse geöffnet werden.

```csharp
// Mit der ComHelper-Klasse können wir Dokumente aus COM-Clients laden.
ComHelper comHelper = new ComHelper();

// 1 – Verwendung eines lokalen Systemdateinamens:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Aus einem Stream:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Siehe auch

* class [ComHelper](../)
* namensraum [Aspose.Words](../../comhelper/)
* Montage [Aspose.Words](../../../)


