---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked yöntemi"
linktitle: "get_Checked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_Checked yöntemi. Checkbox SDT'nin mevcut durumunu Alır/Ayarlar. Bu özelliğin varsayılan değeri C++'ta false'dur."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_checked/
---
## StructuredDocumentTag::get_Checked method


Onay kutusu **SDT**'nin mevcut durumunu alır/ayarlar. Bu özelliğin varsayılan değeri **false**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_Checked()
```

## Açıklamalar


Bu özelliğe erişim yalnızca [Checkbox](../../sdttype/) SDT türleri için çalışır.

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
