---
title: "Aspose::Words::BorderType enum"
linktitle: "BorderType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderType enum. Bir kenarın taraflarını belirtir. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 81000
url: /tr/cpp/aspose.words/bordertype/
---
## BorderType enum


Bir kenarlığın kenarlarını belirtir. Daha fazla bilgi için [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) dokümantasyon makalesini ziyaret edin.

```cpp
enum class BorderType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | -1 | Varsayılan değer. |
| Alt | 0 | Bir paragrafın veya tablo hücresinin alt kenarını belirtir. |
| Sol | 1 | Bir paragrafın veya tablo hücresinin sol kenarını belirtir. |
| Sağ | 2 | Bir paragrafın veya tablo hücresinin sağ kenarını belirtir. |
| Üst | 3 | Bir paragrafın veya tablo hücresinin üst kenarını belirtir. |
| Yatay | 4 | Bir tabloda hücreler arasında veya uyumlu paragraflar arasında yatay kenarı belirtir. |
| Dikey | 5 | Bir tabloda hücreler arasında dikey kenarı belirtir. |
| DiagonalDown | 6 | Bir tablo hücresindeki çapraz kenarı belirtir. |
| DiagonalUp | 7 | Bir tablo hücresindeki çapraz kenarı belirtir. |


## Örnekler



Üst kenarlıklı bir paragrafın nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Border> topBorder = builder->get_ParagraphFormat()->get_Borders()->get_Top();
topBorder->set_LineWidth(4.0);
topBorder->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
// ThemeColor yalnızca LineWidth veya LineStyle ayarlandığında ayarlayın.
topBorder->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
topBorder->set_TintAndShade(0.25);

builder->Writeln(u"Text with a top border.");

doc->Save(get_ArtifactsDir() + u"Border.ParagraphTopBorder.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
