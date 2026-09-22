---
title: "Aspose::Words::DocumentBuilderOptions sınıfı"
linktitle: "DocumentBuilderOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilderOptions sınıfı. C++'ta belge oluşturma süreci için ek seçenekler belirtmeye olanak tanır."
type: docs
weight: 22500
url: /tr/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Belge oluşturma süreci için ek seçenekler belirtmeye izin verir.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa **true** olur. Varsayılan değer **true**'dır. |
| [get_DesignMode](./get_designmode/)() const | Microsoft Word'deki Tasarım Modu'na karşılık gelir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Ayarlayıcı: [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Microsoft Word'deki Tasarım Modu'na karşılık gelir. |
| static [Type](./type/)() |  |

## Örnekler



Tablo biçimlendirmesini sonraki içerik için nasıl yok sayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Tablonun önüne içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Tablonun içindeki yazı tipi boyutunu değiştirir.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi sonraki içeriğe uygulanmaz.
// ContextTableFormatting false ise, tablo biçimlendirmesi sonraki içeriğe uygulanır.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
