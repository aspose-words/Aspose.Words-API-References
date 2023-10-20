---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words für .NET
description: Aspose.Words.ComHelper klas. Stellt Methoden für COMClients zum Laden eines Dokuments in Aspose.Words bereit in C#.
type: docs
weight: 220
url: /de/net/aspose.words/comhelper/
---
## ComHelper class

Stellt Methoden für COM-Clients zum Laden eines Dokuments in Aspose.Words bereit.

```csharp
public class ComHelper
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ComHelper](comhelper/)() | Initialisiert eine neue Instanz dieser Klasse. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Ermöglicht das Laden einer COM-Anwendung[`Document`](../document/) aus einem Stream. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Ermöglicht einer COM-Anwendung das Laden von a[`Document`](../document/) aus einer Datei. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Ermöglicht einer COM-Anwendung das Laden von a[`Document`](../document/) von einem IStream-Objekt. |

## Bemerkungen

Benutzen Sie die`ComHelper` Klasse zum Laden eines Dokuments aus einer Datei oder einem Stream in ein [`Document`](../document/) Objekt in einer COM-Anwendung.

Der[`Document`](../document/) Die Klasse stellt einen Standardkonstruktor zum Erstellen eines neuen Dokuments sowie überladene Konstruktoren zum Laden eines Dokuments aus einer Datei oder einem Stream bereit. Wenn Sie Aspose.Words aus einer .NET-Anwendung verwenden, können Sie alle verwenden[`Document`](../document/) -Konstruktoren direkt, aber wenn Sie Aspose.Words aus einer COM-Anwendung verwenden, nur die Standardeinstellung[`Document`](../document/) Konstruktor ist verfügbar.

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
