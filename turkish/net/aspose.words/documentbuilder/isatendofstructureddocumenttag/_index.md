---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: .NET için Aspose.Words
description: DocumentBuilder'ın IsAtEndOfStructuredDocumentTag özelliğini keşfedin; verimli düzenleme için imlecinizin yapılandırılmış belge etiketinin sonunda konumlanıp konumlanmadığını kontrol edin!
type: docs
weight: 120
url: /tr/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Geri Döndürür**doğru** imleç yapılandırılmış bir belge etiketinin sonundaysa.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
```

## Örnekler

DocumentBuilder imlecinin yapılandırılmış bir belge etiketi içerisinde nasıl hareket ettirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// İmleci hareket ettirmenin birkaç yolu vardır:
// 1 - Dizine göre yapılandırılmış belge etiketinin ilk karakterine git.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - Nesneye göre yapılandırılmış belge etiketinin ilk karakterine git.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - İkinci yapılandırılmış belge etiketinin sonuna git.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Şu anda seçili olan yapılandırılmış belge etiketini al.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
