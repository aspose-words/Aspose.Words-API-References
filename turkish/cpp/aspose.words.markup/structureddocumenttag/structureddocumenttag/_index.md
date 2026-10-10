---
title: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag yapıcı"
linktitle: "StructuredDocumentTag"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag yapıcı. C++'ta Structured document tag sınıfının yeni bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/structureddocumenttag/
---
## StructuredDocumentTag::StructuredDocumentTag constructor


Yeni bir **Structured document tag** sınıfı örneği başlatır.

```cpp
Aspose::Words::Markup::StructuredDocumentTag::StructuredDocumentTag(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Markup::SdtType type, Aspose::Words::Markup::MarkupLevel level)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
| tür | Aspose::Words::Markup::SdtType | SDT düğümünün türü. |
| seviye | Aspose::Words::Markup::MarkupLevel | Belge içindeki SDT düğümünün seviyesi. |
## Açıklamalar


Aşağıdaki SDT türleri oluşturulabilir:

* [Checkbox](../../sdttype/)
* [DropDownList](../../sdttype/)
* [ComboBox](../../sdttype/)
* [Date](../../sdttype/)
* [BuildingBlockGallery](../../sdttype/)
* [Group](../../sdttype/)
* [Picture](../../sdttype/)
* [RichText](../../sdttype/)
* [PlainText](../../sdttype/)



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [SdtType](../../sdttype/)
* Enum [MarkupLevel](../../markuplevel/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
