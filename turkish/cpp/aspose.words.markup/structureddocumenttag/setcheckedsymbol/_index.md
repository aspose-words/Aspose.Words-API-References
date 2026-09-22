---
title: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol metodu"
linktitle: "SetCheckedSymbol"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol metodu. C++ içinde bir onay kutusu içerik denetiminin işaretli durumunu temsil etmek için kullanılan sembolü ayarlar."
type: docs
weight: 58000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/setcheckedsymbol/
---
## StructuredDocumentTag::SetCheckedSymbol method


İşaret kutusu içerik denetiminin işaretli durumunu temsil eden sembolü ayarlar.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::SetCheckedSymbol(int32_t characterCode, const System::String &fontName)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| characterCode | int32_t | Belirtilen sembol için karakter kodu. |
| fontName | const System::String\& | Sembolu içeren yazı tipinin adı. |
## Açıklamalar


Bu metoda erişim yalnızca [Checkbox](../../sdttype/) SDT türleri için çalışır.

Diğer tüm SDT türleri için bir istisna oluşacaktır.

## Örnekler



Bir onay kutusu biçiminde yapılandırılmış belge etiketi oluşturmayı göster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto sdtCheckBox = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
sdtCheckBox->set_Checked(true);

// Bir onay kutusu içerik denetiminin işaretli/işaretsiz durumunu temsil etmek için kullanılan sembolleri ayarlayabiliriz.
sdtCheckBox->SetCheckedSymbol(0x00A9, u"Times New Roman");
sdtCheckBox->SetUncheckedSymbol(0x00AE, u"Times New Roman");

builder->InsertNode(sdtCheckBox);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CheckBox.docx");
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
