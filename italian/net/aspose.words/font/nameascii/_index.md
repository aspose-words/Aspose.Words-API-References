---
title: Font.NameAscii
linktitle: NameAscii
articleTitle: NameAscii
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font NameAscii per personalizzare i font di testo latini, migliorando il tuo design con codici carattere da 0 a 127 per una migliore leggibilità.
type: docs
weight: 240
url: /it/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Restituisce o imposta il font utilizzato per il testo latino (caratteri con codici carattere da 0 (zero) a 127).

```csharp
public string NameAscii { get; set; }
```

## Esempi

Mostra come Microsoft Word può combinare due diversi tipi di carattere in un'unica esecuzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supponiamo di eseguire un'operazione per la quale utilizziamo il builder per inserire durante l'utilizzo di questa configurazione del font
// contiene caratteri compresi nell'intervallo dei caratteri ASCII. In tal caso,
// visualizzerà quei caratteri utilizzando questo font.
builder.Font.NameAscii = "Calibri";

// Se non viene specificato nessun altro font, il builder applicherà questo font a tutti i caratteri che inserirà.
Assert.AreEqual("Calibri", builder.Font.Name);

// Specifica un font da utilizzare per tutti i caratteri esterni all'intervallo ASCII.
// Idealmente, questo font dovrebbe avere un glifo per ogni codice di carattere non ASCII richiesto.
builder.Font.NameOther = "Courier New";

// Inserisce una sequenza con una parola composta da caratteri ASCII e una parola con tutti i caratteri al di fuori di tale intervallo.
// Ogni carattere verrà visualizzato utilizzando uno dei due font, a seconda.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Guarda anche

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
