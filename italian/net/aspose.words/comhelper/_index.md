---
title: ComHelper Class
linktitle: ComHelper
articleTitle: ComHelper
second_title: Aspose.Words per .NET
description: Sblocca l'integrazione perfetta dei documenti con Aspose.Words.ComHelper. Carica e gestisci senza sforzo i documenti per i client COM con potenti funzionalità.
type: docs
weight: 410
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
| [Open](../../aspose.words/comhelper/open/#open_1)(*string*) | Consente a un'applicazione COM di caricare un[`Document`](../document/) da un file. |
| [OpenIStream](../../aspose.words/comhelper/openistream/)(*IStream*) | Consente a un'applicazione COM di caricare un[`Document`](../document/) da un oggetto IStream. |

## Osservazioni

Utilizzare il`ComHelper` classe per caricare un documento da un file o flusso in un [`Document`](../document/) oggetto in un'applicazione COM.

IL[`Document`](../document/) la classe fornisce un costruttore predefinito per creare un nuovo documento e fornisce anche costruttori sovraccarichi per caricare un documento da un file o da un flusso. Se si utilizza Aspose.Words da un'applicazione .NET, è possibile utilizzare tutti i[`Document`](../document/)costruttori direttamente, ma se si utilizza Aspose.Words da un'applicazione COM, solo l'impostazione predefinita[`Document`](../document/) il costruttore è disponibile.

## Esempi

```csharp
[VBScript]

Dim helper
Set helper = CreateObject("Aspose.Words.ComHelper")

Dim doc
Set doc = helper.Open(fileName)
```

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
