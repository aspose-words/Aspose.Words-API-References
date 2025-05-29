---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToStructuredDocumentTag yöntemi ile yapılandırılmış belge etiketlerine zahmetsizce giderek belge düzenleme verimliliğinizi artırın.
type: docs
weight: 620
url: /tr/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

İmleci geçerli bölümdeki yapılandırılmış bir belge etiketine taşır.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | Taşınacak yapılandırılmış belge etiketinin dizini. |
| characterIndex | Int32 | Yapılandırılmış belge etiketinin içindeki karakterin dizini. Negatif bir değer, yapılandırılmış belge etiketinin sonundan itibaren bir konum belirtmenize olanak tanır. Yapılandırılmış belge etiketinin sonuna gitmek için -1 kullanın. Yapılandırılmış belge etiketi blok düzeyindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |

## Notlar

Gezinme, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, the imlecini ilk bölümün birincil başlığına taşıdıysanız, o zaman*structuredDocumentTagIndex* o bölümün başlığının içindeki yapılandırılmış belge etiketinin dizinini belirtti.

Ne zaman*structuredDocumentTagIndex* 0'dan büyük veya ona eşitse, bölümün başlangıcından itibaren 0'ın ilk yapılandırılmış belge etiketi olduğu bir index belirtir. When *structuredDocumentTagIndex*0'dan küçükse, -1'in son yapılandırılmış belge etiketi olduğu the bölümünün sonundan itibaren bir dizin belirtti.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

İmleci yapılandırılmış belge etiketine taşır.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | Taşınacak yapılandırılmış belge etiketi. |
| characterIndex | Int32 | Yapılandırılmış belge etiketinin içindeki karakterin dizini. Negatif bir değer, yapılandırılmış belge etiketinin sonundan itibaren bir konum belirtmenize olanak tanır. Yapılandırılmış belge etiketinin sonuna gitmek için -1 kullanın. Yapılandırılmış belge etiketi blok düzeyindeyse ve imleci son paragrafının sonuna taşımak istiyorsanız, -2 belirtin. |

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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
