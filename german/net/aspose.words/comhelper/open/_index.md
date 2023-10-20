---
title: ComHelper.Open
linktitle: Open
articleTitle: Open
second_title: Aspose.Words für .NET
description: ComHelper Open methode. Ermöglicht einer COMAnwendung das Laden von aDocument aus einer Datei in C#.
type: docs
weight: 20
url: /de/net/aspose.words/comhelper/open/
---
## Open(*string*) {#open_1}

Ermöglicht einer COM-Anwendung das Laden von a[`Document`](../../document/) aus einer Datei.

```csharp
public Document Open(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Dateiname des zu ladenden Dokuments. |

### Rückgabewert

A[`Document`](../../document/)Objekt, das ein Word-Dokument darstellt.

## Bemerkungen

Diese Methode entspricht dem Aufruf von[`Document`](../../document/) Konstruktor mit einem Dateinamenparameter.

## Beispiele

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* class [Document](../../document/)
* class [ComHelper](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## Open(*Stream*) {#open}

Ermöglicht das Laden einer COM-Anwendung[`Document`](../../document/) aus einem Stream.

```csharp
public Document Open(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Ein .NET-Stream-Objekt, das das zu ladende Dokument enthält. |

### Rückgabewert

A[`Document`](../../document/)Objekt, das ein Word-Dokument darstellt.

## Bemerkungen

Diese Methode entspricht dem Aufruf von[`Document`](../../document/) Konstruktor mit einem Stream-Parameter.

## Beispiele

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

* class [Document](../../document/)
* class [ComHelper](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
