---
title: ComHelper.Open
second_title: Aspose.Words per .NET API Reference
description: ComHelper metodo. Consente a unapplicazione COM di caricare aDocument da un file.
type: docs
weight: 20
url: /it/net/aspose.words/comhelper/open/
---
## Open(string) {#open_1}

Consente a un'applicazione COM di caricare a[`Document`](../../document/) da un file.

```csharp
public Document Open(string fileName)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fileName | String | Nome file del documento da caricare. |

### Valore di ritorno

UN[`Document`](../../document/) oggetto che rappresenta un documento di Word.

### Osservazioni

Questo metodo equivale a chiamare il[`Document`](../../document/) costruttore con un parametro del nome file.

### Esempi

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

* class [Document](../../document/)
* class [ComHelper](../)
* spazio dei nomi [Aspose.Words](../../comhelper/)
* assemblea [Aspose.Words](../../../)

---

## Open(Stream) {#open}

Consente il caricamento di un'applicazione COM[`Document`](../../document/) da un flusso.

```csharp
public Document Open(Stream stream)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| stream | Stream | Un oggetto flusso .NET che contiene il documento da caricare. |

### Valore di ritorno

UN[`Document`](../../document/) oggetto che rappresenta un documento di Word.

### Osservazioni

Questo metodo equivale a chiamare il[`Document`](../../document/) costruttore con un parametro di flusso.

### Esempi

Mostra come aprire documenti utilizzando la classe ComHelper.

```csharp
// La classe ComHelper ci consente di caricare documenti dai client COM.
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

* class [Document](../../document/)
* class [ComHelper](../)
* spazio dei nomi [Aspose.Words](../../comhelper/)
* assemblea [Aspose.Words](../../../)


