---
title: Font.NameOther
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Restituisce o imposta il font utilizzato per i caratteri con codici carattere da 128 a 255.
type: docs
weight: 270
url: /it/net/aspose.words/font/nameother/
---
## Font.NameOther property

Restituisce o imposta il font utilizzato per i caratteri con codici carattere da 128 a 255.

```csharp
public string NameOther { get; set; }
```

### Esempi

Mostra come Microsoft Word può combinare due diversi tipi di carattere in un'unica esecuzione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Supponiamo una corsa che utilizziamo il builder per inserire durante l'utilizzo di questa configurazione di font
// contiene caratteri all'interno dell'intervallo di caratteri ASCII. In quel caso,
// visualizzerà quei caratteri usando questo font.
builder.Font.NameAscii = "Calibri";

// Senza nessun altro font specificato, il builder applicherà questo font anche a tutti i caratteri che inserisce.
Assert.AreEqual("Calibri", builder.Font.Name);

// Specifica un carattere da utilizzare per tutti i caratteri al di fuori dell'intervallo ASCII.
// Idealmente, questo font dovrebbe avere un glifo per ogni codice carattere non ASCII richiesto.
builder.Font.NameOther = "Courier New";

// Inserisce una sequenza con una parola composta da caratteri ASCII e una parola con tutti i caratteri al di fuori di tale intervallo.
// Ogni carattere verrà visualizzato utilizzando uno dei caratteri, a seconda di.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Guarda anche

* property [Name](../name/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


