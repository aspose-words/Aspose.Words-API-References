---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words for .NET
description: Document ShowGrammaticalErrors mülk. Bu belgede dilbilgisi hatalarının görüntülenip görüntülenmeyeceğini belirtir C#'da.
type: docs
weight: 390
url: /tr/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Bu belgede dilbilgisi hatalarının görüntülenip görüntülenmeyeceğini belirtir.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Örnekler

Belgedeki hataların nasıl gösterileceğini/gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Alınacak hatalı iki cümleyi ekleyin
// Microsoft Word'deki yazım ve dilbilgisi denetleyicileri tarafından.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Bu seçenekler etkinleştirilirse yazım hatalarının altı çizilir
// çıktı belgesinde pürüzlü bir kırmızı çizgi bulunur ve çift mavi çizgi dilbilgisi hatalarını vurgulayacaktır.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
