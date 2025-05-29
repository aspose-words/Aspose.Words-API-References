---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: .NET için Aspose.Words
description: Belgenizdeki dil bilgisi hatalarının görünürlüğünü ShowGrammaticalErrors özelliğiyle kontrol edin. Yazım netliğini ve profesyonelliği zahmetsizce artırın.
type: docs
weight: 410
url: /tr/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Bu belgede dilbilgisi hatalarının gösterilip gösterilmeyeceğini belirtir.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Örnekler

Belgedeki hataların nasıl gösterileceğini/gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Dikkat çekecek hatalar içeren iki cümle ekleyin
// Microsoft Word'deki yazım ve dilbilgisi denetleyicileri tarafından.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Bu seçenekler etkinleştirilirse, yazım hataları altı çizili olur
// çıktı belgesinde kesik kırmızı bir çizgi ve çift mavi bir çizgi ile dil bilgisi hataları vurgulanacaktır.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
