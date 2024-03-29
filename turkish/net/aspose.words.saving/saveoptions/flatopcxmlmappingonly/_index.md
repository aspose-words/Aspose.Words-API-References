---
title: SaveOptions.FlatOpcXmlMappingOnly
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.XmlMapping . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/saveoptions/flatopcxmlmappingonly/
---
## SaveOptions.FlatOpcXmlMappingOnly property

Hangi belge biçimlerinin eşlenmesine izin verildiğini belirleyen değeri alır veya ayarlar.[`XmlMapping`](../../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Yalnızca varsayılan olarakFlatOpc belge biçiminin eşlenmesine izin verilir.

```csharp
public bool FlatOpcXmlMappingOnly { get; set; }
```

### Notlar

Bu seçenek,[`FlatOpcXmlMappingOnly`](../../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) . İsteğe bağlı belge biçiminin eşlenmesine izin vermek için genellikle ikisini de false olarak ayarlamanız gerekir.

### Örnekler

Yapılandırılmış belge etiketlerinin herhangi bir biçime nasıl bağlanacağını gösterir.

```csharp
// Eğer doğruysa - SDT ham HTML metni içerecektir.
// Yanlışsa - eşlenmiş HTML ayrıştırılacak ve ortaya çıkan belge SDT içeriğine eklenecektir.
LoadOptions loadOptions = new LoadOptions { FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly };
Document doc = new Document(MyDir + "Structured document tag with HTML content.docx", loadOptions);

SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);
saveOptions.FlatOpcXmlMappingOnly = isFlatOpcXmlMappingOnly;

doc.Save(ArtifactsDir + "LoadOptions.FlatOpcXmlMappingOnly.pdf", saveOptions);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


