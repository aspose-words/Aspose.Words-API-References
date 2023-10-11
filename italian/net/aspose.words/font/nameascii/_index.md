---
title: Font.NameAscii
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Restituisce o imposta il carattere utilizzato per il testo latino caratteri con codici carattere da 0 zero a 127.
type: docs
weight: 240
url: /it/net/aspose.words/font/nameascii/
---
## Font.NameAscii property

Restituisce o imposta il carattere utilizzato per il testo latino (caratteri con codici carattere da 0 (zero) a 127).

```csharp
public string NameAscii { get; set; }
```

### Esempi

Mostra come Microsoft Word può combinare due caratteri diversi in un'unica esecuzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supponiamo che venga inserita un'esecuzione che utilizziamo il builder durante l'utilizzo di questa configurazione di carattere
// contiene caratteri compresi nell'intervallo dei caratteri ASCII. In quel caso,
// visualizzerà quei caratteri utilizzando questo carattere.
builder.Font.NameAscii = "Calibri";

// Senza nessun altro carattere specificato, il builder applicherà questo carattere anche a tutti i caratteri che inserisce.
Assert.AreEqual("Calibri", builder.Font.Name);

// Specifica un carattere da utilizzare per tutti i caratteri al di fuori dell'intervallo ASCII.
// Idealmente, questo carattere dovrebbe avere un glifo per ogni codice di carattere non ASCII richiesto.
builder.Font.NameOther = "Courier New";

// Inserisce una sequenza con una parola composta da caratteri ASCII e una parola con tutti i caratteri esterni a tale intervallo.
// Ogni carattere verrà visualizzato utilizzando uno dei caratteri, a seconda.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Guarda anche

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


