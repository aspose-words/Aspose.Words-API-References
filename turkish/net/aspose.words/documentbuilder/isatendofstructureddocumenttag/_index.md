---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder mülk. İadeler doğru imleç yapılandırılmış bir belge etiketinin sonundaysa.
type: docs
weight: 120
url: /tr/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

İadeler **doğru** imleç yapılandırılmış bir belge etiketinin sonundaysa.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
```

### Örnekler

DocumentBuilder imlecinin yapılandırılmış bir belge etiketi içinde nasıl hareket ettirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// İmleci hareket ettirmenin birkaç yolu vardır:
// 1 - Yapılandırılmış belge etiketinin ilk karakterine dizine göre git.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Yapılandırılmış belge etiketinin ilk karakterine nesneye göre git.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - İkinci yapılandırılmış belge etiketinin sonuna git.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// Şu anda seçili olan yapılandırılmış belge etiketini alın.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


