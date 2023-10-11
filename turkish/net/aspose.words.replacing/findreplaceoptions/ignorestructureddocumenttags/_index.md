---
title: FindReplaceOptions.IgnoreStructuredDocumentTags
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. İçeriğin yoksayılacağını belirten bir boole değeri alır veya ayarlar.StructuredDocumentTag . Varsayılan değerYANLIŞ .
type: docs
weight: 120
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/
---
## FindReplaceOptions.IgnoreStructuredDocumentTags property

İçeriğin yoksayılacağını belirten bir boole değeri alır veya ayarlar.[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) . Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreStructuredDocumentTags { get; set; }
```

### Notlar

Bu seçenek olarak ayarlandığında`doğru` , içeriği[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) basit bir metin olarak değerlendirilecektir.

Aksi takdirde,[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) bağımsız Story olarak işlenecek ve değiştirilen desen her biri için ayrı ayrı aranacak[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/), böylece desen bir noktayı geçerse[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , bu durumda böyle bir model için değiştirme gerçekleştirilmeyecektir.

### Örnekler

Etiketlerin içeriğinin değiştirilmeden nasıl yok sayılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

// Bu paragraf SDT'yi içermektedir.
Paragraph p = (Paragraph)doc.FirstSection.Body.GetChild(NodeType.Paragraph, 2, true);
string textToSearch = p.ToString(SaveFormat.Text).Trim();

FindReplaceOptions options = new FindReplaceOptions() { IgnoreStructuredDocumentTags = true };
doc.Range.Replace(textToSearch, "replacement", options);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


