---
title: DocumentBuilder.MoveToStructuredDocumentTag
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci geçerli bölümdeki yapılandırılmış belge etiketine taşır.
type: docs
weight: 590
url: /tr/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(int, int) {#movetostructureddocumenttag_1}

İmleci geçerli bölümdeki yapılandırılmış belge etiketine taşır.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Taşınacak yapılandırılmış belge etiketinin dizini. |
| characterIndex | Int32 | Yapılandırılmış belge etiketinin içindeki karakterin dizini. Negatif bir değer, yapılandırılmış belge etiketinin sonundan itibaren bir konum belirtmenize olanak tanır. Yapılandırılmış belge etiketinin sonuna gitmek için -1 to komutunu kullanın. Yapılandırılmış belge etiketi blok düzeyindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız -2'yi belirtin. |

### Notlar

Gezinme, geçerli bölümün geçerli öyküsü içinde gerçekleştirilir. Yani, the imlecini ilk bölümün birincil başlığına taşıdıysanız, o zaman*structuredDocumentTagIndex* , o bölümün başlığının içindeki yapılandırılmış belge etiketinin dizinini belirtti.

Ne zaman*structuredDocumentTagIndex* 0'dan büyük veya ona eşitse, 0'ın ilk yapılandırılmış belge etiketi olduğu bölümün başından itibaren bir index belirtir. When *structuredDocumentTagIndex* 0'dan küçükse, son yapılandırılmış belge etiketi olan -1 ile the bölümünün sonundan itibaren bir dizin belirtti.

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

---

## MoveToStructuredDocumentTag(StructuredDocumentTag, int) {#movetostructureddocumenttag}

İmleci yapılandırılmış belge etiketine taşır.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Taşınacak yapılandırılmış belge etiketi. |
| characterIndex | Int32 | Yapılandırılmış belge etiketinin içindeki karakterin dizini. Negatif bir değer, yapılandırılmış belge etiketinin sonundan itibaren bir konum belirtmenize olanak tanır. Yapılandırılmış belge etiketinin sonuna gitmek için -1 to komutunu kullanın. Yapılandırılmış belge etiketi blok düzeyindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız -2'yi belirtin. |

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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


