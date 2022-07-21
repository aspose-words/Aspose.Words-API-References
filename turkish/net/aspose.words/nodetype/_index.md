---
title: NodeType
second_title: Aspose.Words for .NET API Referansı
description: Bir Word belge düğümünün türünü belirtir.
type: docs
weight: 3990
url: /tr/net/aspose.words/nodetype/
---
## NodeType enumeration

Bir Word belge düğümünün türünü belirtir.

```csharp
public enum NodeType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Any | `0` | Tüm düğüm türlerini gösterir. Tüm çocukları seçmeye izin verir. |
| Document | `1` | A[`Document`](../document) belge ağacının kökü olarak tüm Word belgesine erişim sağlayan nesne. |
| Section | `2` | A[`Section`](../section) Word belgesindeki bir bölüme karşılık gelen nesne. |
| Body | `3` | A[`Body`](../body) Bir bölümün ana metnini içeren nesne (ana metin öyküsü). |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter) Bir bölümün içinde belirli bir üstbilgi veya altbilginin metnini içeren nesne. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table) Word belgesindeki bir tabloyu temsil eden nesne. |
| Row | `6` | Bir tablo satırı. |
| Cell | `7` | Bir tablo satırının hücresi. |
| Paragraph | `8` | Bir metin paragrafı. |
| BookmarkStart | `9` | Bir yer imi işaretçisinin başlangıcı. |
| BookmarkEnd | `10` | Yer imi işaretçisinin sonu. |
| EditableRangeStart | `11` | Düzenlenebilir bir aralığın başlangıcı. |
| EditableRangeEnd | `12` | Düzenlenebilir bir aralığın sonu. |
| MoveFromRangeStart | `13` | MoveFrom aralığının başlangıcı. |
| MoveFromRangeEnd | `14` | MoveFrom aralığının sonu. |
| MoveToRangeStart | `15` | MoveTo aralığının başlangıcı. |
| MoveToRangeEnd | `16` | MoveTo aralığının sonu. |
| GroupShape | `17` | Bir grup şekil, görüntü, OLE nesnesi veya diğer grup şekilleri. |
| Shape | `18` | OfficeArt şekli, görüntüsü veya OLE nesnesi gibi bir çizim nesnesi. |
| Comment | `19` | Word belgesindeki bir yorum. |
| Footnote | `20` | Word belgesindeki bir dipnot veya son not. |
| Run | `21` | Bir metin akışı. |
| FieldStart | `22` | Bir Word alanının başlangıcını belirten özel bir karakter. |
| FieldSeparator | `23` | Alan kodunu alan sonucundan ayıran özel bir karakter. |
| FieldEnd | `24` | Bir Word alanının sonunu belirten özel bir karakter. |
| FormField | `25` | Bir form alanı. |
| SpecialChar | `26` | Daha spesifik özel karakter türlerinden biri olmayan özel bir karakter. |
| SmartTag | `27` | Bir paragraf içindeki bir veya daha fazla satır içi yapının (çalışmalar, resimler, alanlar, vb.) etrafındaki akıllı etiket |
| StructuredDocumentTag | `28` | Müşteriye özel bilgilerin ve sunum araçlarının tanımlanmasına izin verir. |
| StructuredDocumentTagRangeStart | `29` | bir başlangıç **menzilli** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| StructuredDocumentTagRangeEnd | `30` | bir sonu **menzilli** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| GlossaryDocument | `31` | Ana belge içinde bir sözlük belgesi. |
| BuildingBlock | `32` | Sözlük belgesi içindeki bir yapı taşı (örneğin, sözlük belgesi girişi). |
| CommentRangeStart | `33` | Yorumlanmış bir aralığın başlangıcını temsil eden bir işaretleyici düğüm. |
| CommentRangeEnd | `34` | Yorum yapılan aralığın sonunu temsil eden bir işaretleyici düğüm. |
| OfficeMath | `35` | Bir Office Math nesnesi. Denklem, fonksiyon, matris veya diğer matematiksel nesnelerden biri olabilir. Matematiksel nesne koleksiyonu olabilir ve ayrıca metin dizileri gibi matematiksel olmayan bazı nesneleri içerebilir. |
| SubDocument | `36` | Başka bir belgeye bağlantı olan bir alt belge düğümü. |
| System | `37` | Aspose.Words. tarafından dahili kullanım için ayrılmıştır |
| Null | `38` | Aspose.Words. tarafından dahili kullanım için ayrılmıştır |

### Örnekler

Bileşik bir düğümün alt düğüm koleksiyonunda nasıl geçileceğini gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına alt düğümler olarak iki işlem ve bir şekil ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' bir çıktı dosyasına kaydedilmediğini ve yalnızca düğüm ömrü boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın acil alt öğeleri koleksiyonunu yineleyin,
// ve içinde bulduğumuz tüm koşuları veya şekilleri yazdırın.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
    }
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
