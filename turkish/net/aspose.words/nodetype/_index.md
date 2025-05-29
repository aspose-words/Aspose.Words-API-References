---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: .NET için Aspose.Words
description: Sorunsuz belge işleme için farklı Word belge düğüm türlerini kolayca tanımlamak ve yönetmek amacıyla Aspose.Words.NodeType enum'unu keşfedin.
type: docs
weight: 4920
url: /tr/net/aspose.words/nodetype/
---
## NodeType enumeration

Word belge düğümünün türünü belirtir.

```csharp
public enum NodeType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Any | `0` | Tüm düğüm tiplerini belirtir. Tüm alt düğümleri seçmenize izin verir. |
| Document | `1` | A[`Document`](../document/) Belge ağacının kökü olarak, tüm Word belgesine erişim sağlayan nesne. |
| Section | `2` | A[`Section`](../section/) Word belgesindeki bir bölüme karşılık gelen nesne. |
| Body | `3` | A[`Body`](../body/) Bir bölümün (ana metin öyküsünün) ana metnini içeren nesne. |
| HeaderFooter | `4` | A[`HeaderFooter`](../headerfooter/) Bir bölümün içinde belirli bir üstbilgi veya altbilginin metnini içeren nesne. |
| Table | `5` | A[`Table`](../../aspose.words.tables/table/) Word belgesindeki bir tabloyu temsil eden nesne. |
| Row | `6` | Bir masanın sırası. |
| Cell | `7` | Bir tablo satırının hücresi. |
| Paragraph | `8` | Bir paragraf metin. |
| BookmarkStart | `9` | Bir ayraç işaretinin başlangıcı. |
| BookmarkEnd | `10` | Bir ayraç işaretinin sonu. |
| EditableRangeStart | `11` | Düzenlenebilir bir aralığın başlangıcı. |
| EditableRangeEnd | `12` | Düzenlenebilir bir aralığın sonu. |
| MoveFromRangeStart | `13` | MoveFrom aralığının başlangıcı. |
| MoveFromRangeEnd | `14` | MoveFrom aralığının sonu. |
| MoveToRangeStart | `15` | Bir MoveTo aralığının başlangıcı. |
| MoveToRangeEnd | `16` | MoveTo aralığının sonu. |
| GroupShape | `17` | Bir grup şekil, resim, OLE nesnesi veya diğer grup şekilleri. |
| Shape | `18` | OfficeArt şekli, resmi veya OLE nesnesi gibi bir çizim nesnesi. |
| Comment | `19` | Word belgesindeki bir yorum. |
| Footnote | `20` | Word belgesindeki dipnot veya sonnot. |
| Run | `21` | Bir metin dizisi. |
| FieldStart | `22` | Bir Word alanının başlangıcını belirten özel bir karakter. |
| FieldSeparator | `23` | Alan kodunu alan sonucundan ayıran özel bir karakter. |
| FieldEnd | `24` | Bir Word alanının sonunu belirten özel bir karakter. |
| FormField | `25` | Bir form alanı. |
| SpecialChar | `26` | Daha spesifik özel karakter tiplerinden biri olmayan özel bir karakter. |
| SmartTag | `27` | Bir paragraf içindeki bir veya daha fazla satır içi yapı (çalıştırmalar, resimler, alanlar, vb.) etrafındaki akıllı etiket |
| StructuredDocumentTag | `28` | Müşteriye özel bilgilerin ve bunların sunum biçimlerinin tanımlanmasına olanak tanır. |
| StructuredDocumentTagRangeStart | `29` | Bir başlangıç**menzilli** Çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| StructuredDocumentTagRangeEnd | `30` | Bir sonu**menzilli** Çok bölümlü içeriği kabul eden yapılandırılmış belge etiketi. |
| GlossaryDocument | `31` | Ana belge içerisinde bir sözlük belgesi. |
| BuildingBlock | `32` | Bir sözlük belgesi içindeki bir yapı taşı (örneğin sözlük belgesi girişi). |
| CommentRangeStart | `33` | Yorumlanmış bir aralığın başlangıcını temsil eden bir işaretleyici düğümü. |
| CommentRangeEnd | `34` | Yorumlanmış bir aralığın sonunu temsil eden bir işaretleyici düğümü. |
| OfficeMath | `35` | Bir Office Math nesnesi. Denklem, fonksiyon, matris veya diğer matematiksel nesnelerden biri olabilir. Matematiksel nesnelerin bir koleksiyonu olabilir ve ayrıca metin dizileri gibi bazı matematiksel olmayan nesneleri de içerebilir. |
| SubDocument | `36` | Başka bir belgeye bağlantı olan bir alt belge düğümü. |
| System | `37` | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |
| Null | `38` | Aspose.Words tarafından dahili kullanım için ayrılmıştır. |

## Örnekler

Bir bileşik düğümün alt düğüm koleksiyonunda nasıl dolaşılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına iki çalışma ve bir şekil alt düğüm olarak ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' öğesinin bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün yaşam süresi boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın hemen altındaki alt öğelerin koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz herhangi bir koşuyu veya şekli yazdırırız.
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
