---
title: Style.Remove
second_title: Aspose.Words per .NET API Reference
description: Style metodo. Rimuove lo stile specificato dal documento.
type: docs
weight: 200
url: /it/net/aspose.words/style/remove/
---
## Style.Remove method

Rimuove lo stile specificato dal documento.

```csharp
public void Remove()
```

### Osservazioni

La rimozione dello stile ha i seguenti effetti sul modello del documento:

* Tutti i riferimenti allo stile vengono rimossi dai paragrafi, dalle sequenze e dalle tabelle corrispondenti.
* Se lo stile di base viene rimosso, la sua formattazione viene spostata negli stili secondari.
* Se lo stile da eliminare ha uno stile collegato, verranno eliminati entrambi.

### Esempi

Mostra come creare e applicare uno stile personalizzato.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Ridefinisce automaticamente lo stile.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Applica uno degli stili del documento al paragrafo che il generatore di documenti sta creando.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Rimuove il nostro stile personalizzato dalla raccolta di stili del documento.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Qualsiasi testo che utilizzava uno stile rimosso ripristina la formattazione predefinita.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Guarda anche

* class [Style](../)
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


