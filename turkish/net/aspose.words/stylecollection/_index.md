---
title: Class StyleCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.StyleCollection sınıf. Bir belgede hem yerleşik hem de kullanıcı tanımlı stilleri temsil eden Style nesneleri koleksiyonu.
type: docs
weight: 5840
url: /tr/net/aspose.words/stylecollection/
---
## StyleCollection class

Bir belgede hem yerleşik hem de kullanıcı tanımlı stilleri temsil eden Style nesneleri koleksiyonu.

```csharp
public class StyleCollection : IEnumerable<Style>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/stylecollection/count/) { get; } | Koleksiyondaki stil sayısını alır. |
| [DefaultFont](../../aspose.words/stylecollection/defaultfont/) { get; } | Belge varsayılan metin biçimlendirmesini alır. |
| [DefaultParagraphFormat](../../aspose.words/stylecollection/defaultparagraphformat/) { get; } | Belge varsayılan paragraf biçimlendirmesini alır. |
| [Document](../../aspose.words/stylecollection/document/) { get; } | Sahip belgesini alır. |
| [Item](../../aspose.words/stylecollection/item/) { get; } | Ada veya diğer ada göre bir stil alır. (3 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/stylecollection/add/)(StyleType, string) | Kullanıcı tanımlı yeni bir stil oluşturur ve onu koleksiyona ekler. |
| [AddCopy](../../aspose.words/stylecollection/addcopy/)(Style) | Bu koleksiyona bir stil kopyalar. |
| [ClearQuickStyleGallery](../../aspose.words/stylecollection/clearquickstylegallery/)() | Hızlı Stil Galerisi panelinden tüm stilleri kaldırır. |
| [GetEnumerator](../../aspose.words/stylecollection/getenumerator/)() | Stilleri adlarının alfabetik sırasına göre sıralayacak bir numaralandırıcı nesnesi alır. |

### Örnekler

Liste biçimlendirmeli bir paragraf stilinin nasıl oluşturulacağını ve kullanılacağını gösterir.

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

// Belge oluşturucunun stilini liste biçimlendirmesi olmayan bir stille değiştirin ve başka bir paragraf yazın.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Ayrıca bakınız

* class [Style](../style/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


