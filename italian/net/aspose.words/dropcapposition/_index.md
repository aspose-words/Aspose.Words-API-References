---
title: Enum DropCapPosition
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.DropCapPosition enum. Specifica la posizione del testo del capolettera.
type: docs
weight: 1410
url: /it/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Specifica la posizione del testo del capolettera.

```csharp
public enum DropCapPosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Il paragrafo non ha un capolettera. |
| Normal | `1` | Il capolettera è posizionato all'interno del margine di testo sul paragrafo di ancoraggio. |
| Margin | `2` | Il capolettera è posizionato all'esterno del margine di testo sul paragrafo di ancoraggio. |

### Esempi

Mostra come creare un capolettera.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un paragrafo con una lettera grande con cui inizia il testo nel secondo e terzo paragrafo.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Attualmente, il secondo e il terzo paragrafo appariranno sotto il primo.
// Possiamo convertire il primo paragrafo come capolettera per gli altri paragrafi tramite il suo oggetto "ParagraphFormat".
// Imposta la proprietà "DropCapPosition" su "DropCapPosition.Margin" per posizionare il capolettera
// fuori dal margine sinistro della pagina se il nostro testo è da sinistra a destra.
// Imposta la proprietà "DropCapPosition" su "DropCapPosition.Normal" per posizionare il capolettera all'interno dei margini della pagina
// e per avvolgerlo attorno al resto del testo.
// "DropCapPosition.None" è lo stato predefinito per tutti i paragrafi.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


