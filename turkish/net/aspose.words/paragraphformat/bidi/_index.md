---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik ve iyileştirilmiş belge düzeni için sağdan sola metin biçimlendirmesini kolayca kontrol etmek amacıyla ParagraphFormat Bidi özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

Bunun sağdan sola bir paragraf olup olmadığını alır veya ayarlar.

```csharp
public bool Bidi { get; set; }
```

## Notlar

Ne zaman`doğru`, bu paragraph içindeki koşular ve diğer satır içi nesneler sağdan sola doğru düzenlenmiştir.

## Örnekler

Düz metin belge metin yönünün nasıl tespit edileceğini gösterir.

```csharp
// Bir belgenin oluşturucusuna geçirebileceğimiz bir "TxtLoadOptions" nesnesi oluşturun
// düz metin belgenin nasıl yükleneceğini değiştirmek için.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// "DocumentDirection" özelliğini "DocumentDirection.Auto" olarak ayarlayın, otomatik olarak algılar
// Aspose.Words'ün düz metinden yüklediği her metin paragrafının yönü.
// Her paragrafın "Bidi" özelliği onun yönünü saklayacaktır.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// İbranice metni sağdan sola olarak algıla.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// İngilizce metni sağdan sola doğru algıla.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

BIDIOUTLINE alanlarıyla sağdan sola dil uyumlu listelerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE alanı paragrafları AUTONUM/LISTNUM alanları gibi numaralandırır,
// ancak yalnızca İbranice veya Arapça gibi sağdan sola düzenleme dili etkinleştirildiğinde görünür.
// Aşağıdaki alan, liste numarası "1."in RTL karşılığı olan ".1"i gösterecektir.
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// ".2" ve ".3" görüntüleyecek iki adet BIDIOUTLINE alanı daha ekleyin.
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Belgedeki her paragrafın yatay metin hizalamasını RTL olarak ayarlayın.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Microsoft Word'de sağdan sola düzenleme dilini etkinleştirirsek alanlarımız sayılar görüntüler.
// Aksi takdirde "###" görüntülenir.
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
