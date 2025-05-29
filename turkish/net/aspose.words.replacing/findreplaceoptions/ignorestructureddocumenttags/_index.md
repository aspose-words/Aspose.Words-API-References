---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
linktitle: IgnoreStructuredDocumentTags
articleTitle: IgnoreStructuredDocumentTags
second_title: .NET için Aspose.Words
description: FindReplaceOptions IgnoreStructuredDocumentTags özelliğini keşfedin. Bu kullanımı kolay boolean ayarıyla StructuredDocumentTag içeriğinin yoksayılıp yoksayılmayacağını kontrol edin.
type: docs
weight: 120
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

İçeriği yoksaymayı belirten bir Boole değeri alır veya ayarlar[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

## Notlar

Bu seçenek olarak ayarlandığında`doğru` , içeriği[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) basit bir metin olarak ele alınacaktır.

Aksi takdirde,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) bağımsız Story olarak işlenecek ve her biri için değiştirme deseni ayrı ayrı aranacaktır[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , böylece desen bir çizgiyi geçerse[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , o zaman bu desen için değiştirme yapılmayacaktır.

## Örnekler

Değiştirmeden etiket içeriğinin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Bu paragraf SDT içermektedir.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
