---
title: Enum NodeType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.NodeType Sıralama. Word belgesi düğümünün türünü belirtir.
type: docs
weight: 4230
url: /tr/net/aspose.words/nodetype/
---
## NodeType enumeration

Word belgesi düğümünün türünü belirtir.

```csharp
public enum NodeType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Any | `0` | Tüm düğüm türlerini belirtir. Tüm çocukların seçilmesine izin verir. |
| Document | `1` | A[`Document`](../document/) Belge ağacının kökü olarak , Word belgesinin tamamına erişim sağlayan nesne. |
| Section | `2` | A[`Section`](../section/) Word belgesindeki bir bölüme karşılık gelen nesne. |
| Body | `3` | A[`Body`](../body/) Bir bölümün ana metnini (ana metin öyküsü) içeren nesne. |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) Bir bölümün içindeki belirli bir üstbilgi veya altbilginin metnini içeren nesne. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) Word belgesindeki bir tabloyu temsil eden nesne. |
| Row | `6` | Bir sıra masa. |
| Cell | `7` | Bir tablo satırının hücresi. |
| Paragraph | `8` | Bir paragraf metin. |
| BookmarkStart | `9` | Yer imi işaretçisinin başlangıcı. |
| BookmarkEnd | `10` | Yer imi işaretçisinin sonu. |
| EditableRangeStart | `11` | Düzenlenebilir bir aralığın başlangıcı. |
| EditableRangeEnd | `12` | Düzenlenebilir aralığın sonu. |
| MoveFromRangeStart | `13` | MoveFrom serisinin başlangıcı. |
| MoveFromRangeEnd | `14` | MoveFrom aralığının sonu. |
| MoveToRangeStart | `15` | MoveTo serisinin başlangıcı. |
| MoveToRangeEnd | `16` | MoveTo aralığının sonu. |
| GroupShape | `17` | Bir grup şekil, görüntü, OLE nesnesi veya diğer grup şekilleri. |
| Shape | `18` | OfficeArt şekli, görüntüsü veya OLE nesnesi gibi bir çizim nesnesi. |
| Comment | `19` | Bir Word belgesindeki yorum. |
| Footnote | `20` | Word belgesindeki dipnot veya son not. |
| Run | `21` | Bir metin dizisi. |
| FieldStart | `22` | Bir Word alanının başlangıcını belirten özel bir karakter. |
| FieldSeparator | `23` | Alan kodunu alan sonucundan ayıran özel karakter. |
| FieldEnd | `24` | Word alanının sonunu belirten özel bir karakter. |
| FormField | `25` | Bir form alanı. |
| SpecialChar | `26` | Daha spesifik özel karakter türlerinden biri olmayan özel bir karakter. |
| SmartTag | `27` | Bir paragraf içindeki bir veya daha fazla satır içi yapıyı (çalışmalar, resimler, alanlar vb.) çevreleyen akıllı etiket |
| StructuredDocumentTag | `28` | Müşteriye özel bilgilerin ve sunum araçlarının tanımlanmasına olanak sağlar. |
| StructuredDocumentTagRangeStart | `29` | Bir başlangıç **aralıklı** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| StructuredDocumentTagRangeEnd | `30` | bir sonu **aralıklı** çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| GlossaryDocument | `31` | Ana belge içindeki bir sözlük belgesi. |
| BuildingBlock | `32` | Bir sözlük belgesindeki yapı taşı (örneğin sözlük belgesi girişi). |
| CommentRangeStart | `33` | Yorumlanmış bir aralığın başlangıcını temsil eden bir işaretleyici düğüm. |
| CommentRangeEnd | `34` | Yorumlanmış bir aralığın sonunu temsil eden bir işaretleyici düğüm. |
| OfficeMath | `35` | Bir Office Math nesnesi. Denklem, fonksiyon, matris veya diğer matematiksel nesnelerden biri olabilir. Matematiksel nesnelerin bir koleksiyonu olabilir ve ayrıca metin dizileri gibi matematiksel olmayan bazı nesneleri de içerebilir. |
| SubDocument | `36` | Başka bir belgeye bağlantı olan bir alt belge düğümü. |
| System | `37` | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |
| Null | `38` | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |

### Örnekler

Bileşik bir düğümün alt düğüm koleksiyonunda nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına alt düğümler olarak iki işlem ve bir şekil ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId'in bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün ömrü boyunca mevcut olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın yakın alt öğelerinin toplanması yoluyla yineleme yapın,
// ve içinde bulduğumuz tüm sayıları veya şekilleri yazdırıyoruz.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

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
            break;
    }
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


