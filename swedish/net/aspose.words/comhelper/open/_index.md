---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words för .NET
description: ComHelper Open metod. Tillåter en COMapplikation att ladda enDocument från en fil i C#.
type: docs
weight: 20
url: /sv/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Tillåter en COM-applikation att ladda en[`Document`](../../document/) från en fil.

```csharp
public Document Open(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamn på dokumentet som ska laddas. |

### Returvärde

A[`Document`](../../document/)objekt som representerar ett Word-dokument.

## Anmärkningar

Denna metod är samma som att anropa[`Document`](../../document/) konstruktor med en filnamnsparameter.

## Exempel

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Visar hur man öppnar dokument med ComHelper-klassen.

```csharp
// ComHelper-klassen tillåter oss att ladda dokument från COM-klienter.
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

* class [Document](../../document/)
* class [ComHelper](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Tillåter att en COM-applikation laddas[`Document`](../../document/) från en ström.

```csharp
public Document Open(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Ett .NET-strömobjekt som innehåller dokumentet som ska laddas. |

### Returvärde

A[`Document`](../../document/)objekt som representerar ett Word-dokument.

## Anmärkningar

Denna metod är samma som att anropa[`Document`](../../document/) konstruktör med en strömparameter.

## Exempel

Visar hur man öppnar dokument med ComHelper-klassen.

```csharp
// ComHelper-klassen tillåter oss att ladda dokument från COM-klienter.
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

* class [Document](../../document/)
* class [ComHelper](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
