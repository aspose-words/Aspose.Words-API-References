---
title: Font.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words for .NET
description: Font Style mülk. Bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar C#'da.
type: docs
weight: 400
url: /tr/net/aspose.words/font/style/
---
## Font.Style property

Bu biçimlendirmeye uygulanan karakter stilini alır veya ayarlar.

```csharp
public Style Style { get; set; }
```

## Örnekler

Özel karakter stilleriyle biçimlendirilmiş bir belgedeki tüm çalıştırmalara çift alt çizgi uygular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Özel bir stil ekleyin ve bunu belge oluşturucu kullanılarak oluşturulan metne uygulayın.
Style style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Red;
style.Font.Name = "Courier New";

builder.Font.StyleName = "MyStyle";
builder.Write("This text is in a custom style.");

// Her çalıştırmayı yineleyin ve her özel stile çift alt çizgi ekleyin.
foreach (Run run in doc.GetChildNodes(NodeType.Run, true).OfType<Run>())
{
    Style charStyle = run.Font.Style;

    if (!charStyle.BuiltIn)
        run.Font.Underline = Underline.Double;
}

doc.Save(ArtifactsDir + "Font.Style.docx");
```

### Ayrıca bakınız

* class [Style](../../style/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
