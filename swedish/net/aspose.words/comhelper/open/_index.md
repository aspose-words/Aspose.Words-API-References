---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words för .NET
description: Lås upp sömlös integration med ComHelpers Open-metod, vilket möjliggör enkel dokumentinläsning från filer för dina COM-applikationer.
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

En[`Document`](../../document/) objekt som representerar ett Word-dokument.

## Anmärkningar

Den här metoden är densamma som att anropa[`Document`](../../document/) konstruktor med en filnamnsparameter.

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
| stream | Stream | Ett .NET Stream-objekt som innehåller dokumentet som ska läsas in. |

### Returvärde

En[`Document`](../../document/) objekt som representerar ett Word-dokument.

## Anmärkningar

Den här metoden är densamma som att anropa[`Document`](../../document/) konstruktor med en strömparameter.

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

* class [Document](../../document/)
* class [ComHelper](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
