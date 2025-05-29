---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: .NET için Aspose.Words
description: Belgenizdeki yazım hatası görünürlüğünü ShowSpellingErrors özelliğiyle kontrol edin. Düzenleme sürecinizi geliştirin ve belge kalitenizi iyileştirin.
type: docs
weight: 420
url: /tr/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Bu belgede yazım hatalarının gösterilip gösterilmeyeceğini belirtir.

```csharp
public bool ShowSpellingErrors { get; set; }
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
