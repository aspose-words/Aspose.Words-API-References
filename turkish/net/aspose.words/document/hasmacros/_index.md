---
title: Document.HasMacros
linktitle: HasMacros
articleTitle: HasMacros
second_title: .NET için Aspose.Words
description: Belgenizin HasMacros özelliğiyle VBA proje makroları içerip içermediğini keşfedin. İş akışlarınızda otomasyonu ve verimliliği bugün artırın!
type: docs
weight: 200
url: /tr/net/aspose.words/document/hasmacros/
---
## Document.HasMacros property

Geri Döndürür`doğru` eğer belgenin bir VBA projesi varsa (makrolar).

```csharp
public bool HasMacros { get; }
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

* method [RemoveMacros](../removemacros/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
