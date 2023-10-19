---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words for .NET
description: DocumentBuilder CurrentStructuredDocumentTag mülk. Şu anda seçili olan yapılandırılmış belge etiketini alır.DocumentBuilder  C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Şu anda seçili olan yapılandırılmış belge etiketini alır.[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Örnekler

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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
