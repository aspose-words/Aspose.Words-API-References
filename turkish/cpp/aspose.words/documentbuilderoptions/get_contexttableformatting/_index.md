---
title: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting yöntemi"
linktitle: "get_ContextTableFormatting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting yöntemi. Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa true döner. Varsayılan değer C++'ta true'dur."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Tablo içeriğine uygulanan biçimlendirme, ardından gelen içeriğin biçimlendirmesini etkilemiyorsa **true** olur. Varsayılan değer **true**'dır.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


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

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
