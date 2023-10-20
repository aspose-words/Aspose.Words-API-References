---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words per .NET
description: TxtSaveOptions SimplifyListLabels proprietà. Specifica se il programma deve semplificare le etichette dellelenco nel caso in cui la formattazione complessa delle etichette non sia adeguatamente rappresentata da testo semplice in C#.
type: docs
weight: 70
url: /it/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Specifica se il programma deve semplificare le etichette dell'elenco nel caso in cui la formattazione complessa delle etichette non sia adeguatamente rappresentata da testo semplice.

Se impostato su`VERO` , le etichette degli elenchi numerati sono scritte in formato numerico semplice e le etichette degli elenchi dettagliati come semplici caratteri ASCII. Il valore predefinito è`falso`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Esempi

Mostra come modificare l'aspetto degli elenchi quando si salva un documento in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un elenco puntato con cinque livelli di rientro.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "SimplifyListLabels" su "true" per convertire alcuni elenchi
// simboli in caratteri ASCII più semplici, come '*', 'o', '+', '>', ecc.
// Imposta la proprietà "SimplifyListLabels" su "false" per preservare il maggior numero possibile di simboli dell'elenco originale.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

if (simplifyListLabels)
    Assert.AreEqual("* Item 1\r\n" +
                    "  > Item 2\r\n" +
                    "    + Item 3\r\n" +
                    "      - Item 4\r\n" +
                    "        o Item 5\r\n", docText);
else
    Assert.AreEqual("· Item 1\r\n" +
                    "o Item 2\r\n" +
                    "§ Item 3\r\n" +
                    "· Item 4\r\n" +
                    "o Item 5\r\n", docText);
```

### Guarda anche

* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
