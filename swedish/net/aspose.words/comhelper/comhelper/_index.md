---
title: ComHelper
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words för .NET
description: Upptäck ComHelper, den kraftfulla konstruktorn som enkelt initierar nya klassinstanser, vilket förbättrar din programmeringseffektivitet och produktivitet.
type: docs
weight: 10
url: /sv/net/aspose.words/comhelper/comhelper/
---
## ComHelper constructor

Initierar en ny instans av den här klassen.

```csharp
public ComHelper()
```

## Exempel

Visar hur man öppnar dokument med hjälp av ComHelper-klassen.

```csharp
// ComHelper-klassen låter oss läsa in dokument inifrån COM-klienter.
ComHelper comHelper = new ComHelper();

// 1 - Använda ett lokalt systemfilnamn:
Document doc = comHelper.Open(MyDir + "Document.docx");

Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// 2 - Från en ström:
using (FileStream stream = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    doc = comHelper.Open(stream);

    Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());
}
```

### Se även

* class [ComHelper](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
