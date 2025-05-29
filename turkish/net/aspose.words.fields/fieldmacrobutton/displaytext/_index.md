---
title: FieldMacroButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: .NET için Aspose.Words
description: Gelişmiş makro yürütme için FieldMacroButton DisplayText özelliğini nasıl özelleştireceğinizi keşfedin. Sorunsuz kullanıcı komutları için mükemmel düğme metnini ayarlayın!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldmacrobutton/displaytext/
---
## FieldMacroButton.DisplayText property

Makroyu veya komutu çalıştırmak için seçilen "düğme" olarak görünecek metni alır veya ayarlar.

```csharp
public string DisplayText { get; set; }
```

## Örnekler

Bir belgenin makrolarını tıklayarak çalıştırmamızı sağlayan MACROBUTTON alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Bir MACROBUTTON alanı ekleyin ve MacroName özelliğinde belgenin makrolarından birine adıyla başvurun.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Microsoft Word ile birlikte gelen bir makro olan "ViewZoom200"e başvurmak için özelliği kullanın.
// Diğer tüm makrolara Görünüm -> Makrolar (açılır liste) -> Makroları Görüntüle yoluyla ulaşabiliriz.
// Bu menüde "Makrolar:" açılır menüsünden "Word Komutları"nı seçin.
// Belgemiz stok makro ile aynı adı taşıyan özel bir makro içeriyorsa,
// bizim makromuz MACROBUTTON alanının çalıştıracağı makro olacaktır.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Belgeyi makro etkinleştirilmiş belge türü olarak kaydedin.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Ayrıca bakınız

* class [FieldMacroButton](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
