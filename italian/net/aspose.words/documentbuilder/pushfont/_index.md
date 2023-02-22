---
title: DocumentBuilder.PushFont
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder metodo. Salva la formattazione del carattere corrente nello stack.
type: docs
weight: 570
url: /it/net/aspose.words/documentbuilder/pushfont/
---
## DocumentBuilder.PushFont method

Salva la formattazione del carattere corrente nello stack.

```csharp
public void PushFont()
```

### Esempi

Mostra come utilizzare lo stack di formattazione di un generatore di documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta la formattazione del carattere, quindi scrivi il testo che precede il collegamento ipertestuale.
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// Conserva la nostra attuale configurazione di formattazione nello stack.
builder.PushFont();

// Modifica la formattazione corrente del builder applicando un nuovo stile.
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// Ripristina la formattazione del carattere che abbiamo salvato in precedenza e rimuovi l'elemento dallo stack.
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### Guarda anche

* property [Font](../font/)
* method [PopFont](../popfont/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


