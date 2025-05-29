---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words per .NET
description: Scopri come la funzionalità SimplifyListLabels di TxtSaveOptions migliora la chiarezza semplificando le etichette di elenchi complessi per una migliore rappresentazione del testo.
type: docs
weight: 70
url: /it/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Specifica se il programma deve semplificare le etichette degli elenchi nel caso in cui la formattazione complessa delle etichette non venga rappresentata adeguatamente dal testo normale.

Se impostato su`VERO` , le etichette degli elenchi numerati sono scritte nel semplice formato numerico e le etichette degli elenchi dettagliati come semplici caratteri ASCII. Il valore predefinito è`falso`.

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

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "SimplifyListLabels" su "true" per convertire un elenco
// simboli in caratteri ASCII più semplici, come '*', 'o', '+', '>', ecc.
// Impostare la proprietà "SimplifyListLabels" su "false" per preservare quanti più simboli di elenco originali possibili.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Guarda anche

* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
