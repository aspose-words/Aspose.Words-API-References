---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words für .NET
description: Entdecken Sie ComHelper, den leistungsstarken Konstruktor, der mühelos neue Klasseninstanzen initialisiert und so Ihre Programmiereffizienz und Produktivität steigert.
type: docs
weight: 10
url: /de/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public ComHelper()
```

## Beispiele

Zeigt, wie Dokumente mit der ComHelper-Klasse geöffnet werden.

```csharp
// Die ComHelper-Klasse ermöglicht uns, Dokumente aus COM-Clients zu laden.
ComHelper comHelper = new ComHelper();

// 1 – Verwenden eines lokalen Systemdateinamens:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
