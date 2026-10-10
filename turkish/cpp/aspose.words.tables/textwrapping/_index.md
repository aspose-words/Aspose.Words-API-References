---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::TextWrapping enum. C++'da metnin tablo etrafında nasıl sarıldığını belirtir."
type: docs
weight: 16000
url: /tr/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


Metnin tablonun etrafına nasıl sarılacağını belirtir.

```cpp
enum class TextWrapping
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Metin ve tablo, belgede göründükleri sırayla görüntülenir. |
| Etrafında | 1 | Metin, mevcut yan boşluğu kaplayarak tablo etrafında sarılır. |
| Default | n/a | Varsayılan değer. |


## Örnekler



Tablo metin sarma ile nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Tablonun metni etrafında sarmasını sağlamak için "TextWrapping" özelliğini "TextWrapping.Around" olarak ayarlayın,
// ve konumu ayarlayarak onu aşağıdaki paragraf içine ittirin.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
