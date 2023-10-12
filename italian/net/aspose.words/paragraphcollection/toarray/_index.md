---
title: ParagraphCollection.ToArray
second_title: Aspose.Words per .NET API Reference
description: ParagraphCollection metodo. Copia tutti i paragrafi dalla raccolta in un nuovo array di paragrafi.
type: docs
weight: 20
url: /it/net/aspose.words/paragraphcollection/toarray/
---
## ParagraphCollection.ToArray method

Copia tutti i paragrafi dalla raccolta in un nuovo array di paragrafi.

```csharp
public Paragraph[] ToArray()
```

### Valore di ritorno

Una serie di paragrafi.

### Esempi

Mostra come creare una matrice da una NodeCollection.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

Paragraph[] paras = doc.FirstSection.Body.Paragraphs.ToArray();

Assert.AreEqual(22, paras.Length);
```

Mostra come utilizzare la "rimozione a caldo" per rimuovere un nodo durante l'enumerazione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("The first paragraph");
builder.Writeln("The second paragraph");
builder.Writeln("The third paragraph");
builder.Writeln("The fourth paragraph");

// Rimuove un nodo dalla raccolta nel mezzo di un'enumerazione.
foreach (Paragraph para in doc.FirstSection.Body.Paragraphs.ToArray())
    if (para.Range.Text.Contains("third"))
        para.Remove();

Assert.False(doc.GetText().Contains("The third paragraph"));
```

### Guarda anche

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* spazio dei nomi [Aspose.Words](../../paragraphcollection/)
* assemblea [Aspose.Words](../../../)


