---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words för .NET
description: Lås upp sömlös dokumentintegration med Aspose.Words.ComHelper. Ladda och hantera dokument för COM-klienter enkelt med kraftfulla funktioner.
type: docs
weight: 410
url: /sv/net/aspose.words/comhelper/
---
## ComHelper class

Tillhandahåller metoder för COM-klienter att läsa in ett dokument i Aspose.Words.

```csharp
public class ComHelper
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [ComHelper](comhelper/)() | Initierar en ny instans av den här klassen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Tillåter att en COM-applikation laddas[`Document`](../document/) från en ström. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Tillåter en COM-applikation att ladda en[`Document`](../document/) från en fil. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Tillåter en COM-applikation att ladda en[`Document`](../document/) från ett IStream-objekt. |

## Anmärkningar

Använd`ComHelper` klass för att ladda ett dokument från en fil eller ström till en [`Document`](../document/) objekt i en COM-applikation.

De[`Document`](../document/) Klassen tillhandahåller en standardkonstruktor för att skapa ett nytt dokument och tillhandahåller även överbelastade konstruktorer för att läsa in ett dokument från en fil eller ström. Om du använder Aspose.Words från ett .NET-program kan du använda alla[`Document`](../document/) konstruktorer direkt, men om du använder Aspose.Words från en COM-applikation, endast standardvärdet[`Document`](../document/) konstruktören är tillgänglig.

## Exempel

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
