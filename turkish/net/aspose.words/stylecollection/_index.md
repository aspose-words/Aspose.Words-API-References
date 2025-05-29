---
title: StyleCollection Class
linktitle: StyleCollection
articleTitle: StyleCollection
second_title: .NET için Aspose.Words
description: Belgenizin biçimlendirmesini ve tasarımını geliştirmek için zengin bir yerleşik ve özel stil nesneleri dizisine sahip Aspose.Words.StyleCollection sınıfını keşfedin.
type: docs
weight: 6990
url: /tr/net/aspose.words/stylecollection/
---
## StyleCollection class

Bir koleksiyon[`Style`](../style/)bir belgedeki hem yerleşik hem de kullanıcı tanımlı stilleri temsil eden nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Stiller ve Temalarla Çalışma](https://docs.aspose.com/words/net/working-with-styles-and-themes/) belgeleme makalesi.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Koleksiyondaki stil sayısını alır. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Belgenin varsayılan metin biçimlendirmesini alır. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Belgenin varsayılan paragraf biçimlendirmesini alır. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Sahip belgesini alır. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Adına veya takma adına göre bir stil alır. (3 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(*[StyleType](../styletype/), string*) | Yeni bir kullanıcı tanımlı stil oluşturur ve bunu koleksiyona ekler. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(*[Style](../style/)*) | Bu koleksiyona bir stil kopyalar. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Hızlı Stil Galerisi panelinden tüm stilleri kaldırır. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Stilleri adlarının alfabetik sırasına göre numaralandıracak bir numaralandırıcı nesnesi alır. |

## Örnekler

Liste biçimlendirmesiyle bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Özel bir paragraf stili oluşturun.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Bir liste oluşturun ve bu stili kullanan paragrafların bu listeyi kullanacağından emin olun.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Paragraf stilini belge oluşturucunun geçerli paragrafına uygulayın ve ardından biraz metin ekleyin.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stile değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ayrıca bakınız

* class [Style](../style/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
