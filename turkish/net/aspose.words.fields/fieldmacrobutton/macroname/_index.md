---
title: FieldMacroButton.MacroName
second_title: Aspose.Words for .NET API Referansı
description: FieldMacroButton mülk. Çalıştırılacak makronun veya komutun adını alır veya ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldmacrobutton/macroname/
---
## FieldMacroButton.MacroName property

Çalıştırılacak makronun veya komutun adını alır veya ayarlar.

```csharp
public string MacroName { get; set; }
```

### Örnekler

Tıklayarak bir belgenin makrolarını çalıştırmamıza izin vermek için MACROBUTTON alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Macro.docm");
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.IsTrue(doc.HasMacros);

// Bir MACROBUTTON alanı ekleyin ve MacroName özelliğinde belgenin makrolarından birine ada göre başvurun.
FieldMacroButton field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "MyMacro";
field.DisplayText = "Double click to run macro: " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  MyMacro Double click to run macro: MyMacro", field.GetFieldCode());

// Microsoft Word ile birlikte gelen bir makro olan "ViewZoom200"e başvuruda bulunmak için bu özelliği kullanın.
// Diğer tüm makroları Görünüm -> aracılığıyla bulabiliriz. Makrolar (açılır menü) -> Makroları Görüntüle.
// Bu menüde, "Makrolar:" açılır menüsünden "Word Komutları"nı seçin.
// Belgemiz hisse senedi makrosu ile aynı isimde özel bir makro içeriyorsa,
// makromuz MACROBUTTON alanının çalıştırdığı makro olacaktır.
builder.InsertParagraph();
field = (FieldMacroButton)builder.InsertField(FieldType.FieldMacroButton, true);
field.MacroName = "ViewZoom200";
field.DisplayText = "Run " + field.MacroName;

Assert.AreEqual(" MACROBUTTON  ViewZoom200 Run ViewZoom200", field.GetFieldCode());

// Belgeyi makro etkin belge türü olarak kaydedin.
doc.Save(ArtifactsDir + "Field.MACROBUTTON.docm");
```

### Ayrıca bakınız

* class [FieldMacroButton](../)
* ad alanı [Aspose.Words.Fields](../../fieldmacrobutton/)
* toplantı [Aspose.Words](../../../)


