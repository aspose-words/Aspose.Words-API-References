---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words per .NET
description: Aspose.Words.ComHelper classe. Fornisce metodi per i client COM per caricare un documento in Aspose.Words in C#.
type: docs
weight: 220
url: /it/net/aspose.words/comhelper/
---
## ComHelper class

Fornisce metodi per i client COM per caricare un documento in Aspose.Words.

```csharp
public class ComHelper
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ComHelper](comhelper/)() | Inizializza una nuova istanza di questa classe. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Open](../../aspose.words/comhelper/open/#open)(*Stream*) | Consente il caricamento di un'applicazione COM[`Document`](../document/) da un flusso. |
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Consente a un'applicazione COM di caricare a[`Document`](../document/) da un file. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Consente a un'applicazione COM di caricare a[`Document`](../document/) da un oggetto IStream. |

## Osservazioni

Usa il`ComHelper` classe per caricare un documento da un file o eseguire uno streaming in un [`Document`](../document/) oggetto in un'applicazione COM.

IL[`Document`](../document/) fornisce un costruttore predefinito per creare un nuovo document e fornisce anche costruttori sovraccarichi per caricare un documento da un file o stream. Se stai utilizzando Aspose.Words da un'applicazione .NET, puoi utilizzare tutti i[`Document`](../document/) costruttori direttamente, ma se stai utilizzando Aspose.Words da un'applicazione COM, solo il valore predefinito[`Document`](../document/) il costruttore è disponibile.

## Esempi

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

Mostra come aprire documenti utilizzando la classe ComHelper.

```csharp
// La classe ComHelper ci consente di caricare documenti dai client COM.
ComHelper comHelper = new ComHelper();

// 1 - Utilizzando un nome file di sistema locale:
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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
