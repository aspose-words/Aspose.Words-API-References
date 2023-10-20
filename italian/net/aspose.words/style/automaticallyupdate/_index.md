---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words per .NET
description: Style AutomaticallyUpdate proprietà. Specifica se questo stile viene ridefinito automaticamente in base al valore appropriato in C#.
type: docs
weight: 20
url: /it/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

Specifica se questo stile viene ridefinito automaticamente in base al valore appropriato.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## Osservazioni

Se il valore della proprietà è impostato su true, MS Word ridefinisce automaticamente lo stile corrente quando viene modificata la formattazione del paragrafo appropriato.

La proprietà AutomaticallyUpdate è applicabile solo agli stili di paragrafo.

Il valore predefinito è`falso`.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
