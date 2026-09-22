---
title: "Aspose::Words::Layout::RevisionColor enum"
linktitle: "RevisionColor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::RevisionColor enum. C++'ta belge revizyonlarının rengini belirtmeye olanak tanır."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Belge revizyonlarının rengini belirtmeyi sağlar.

```cpp
enum class RevisionColor
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 0 | Varsayılan. |
| Siyah | 1 | 000000 rengini temsil eder. |
| Mavi | 2 | 2e97d3 rengini temsil eder. |
| BrightGreen | 3 | 84a35b rengini temsil eder. |
| ClassicBlue | 4 | 0000ff rengini temsil eder. |
| ClassicRed | 5 | ff0000 rengini temsil eder. |
| DarkBlue | 6 | 376e96 rengini temsil eder. |
| DarkRed | 7 | 881824 rengini temsil eder. |
| DarkYellow | 8 | e09a2b rengini temsil eder. |
| Gray25 | 9 | a0a3a9 rengi temsil eder. |
| Gray50 | 10 | 50565e rengi temsil eder. |
| Green | 11 | 2c6234 rengi temsil eder. |
| Pink | 12 | ce338f rengi temsil eder. |
| Red | 13 | b5082e rengi temsil eder. |
| Teal | 14 | 1b9cab rengi temsil eder. |
| Turquoise | 15 | 3eafc2 rengi temsil eder. |
| Violet | 16 | 633277 rengi temsil eder. |
| White | 17 | ffffff rengi temsil eder. |
| Yellow | 18 | fad272 rengi temsil eder. |
| LightPink | 19 | fce6f4 rengi temsil eder. |
| LightBlue | 20 | e1f2fa rengi temsil eder. |
| LightYellow | 21 | fef4de rengi temsil eder. |
| LightPurple | 22 | eadfef rengini temsil eder. |
| LightOrange | 23 | fce3d0 rengini temsil eder. |
| LightGreen | 24 | e9f8ce rengini temsil eder. |
| Gray | 25 | efeded rengini temsil eder. |
| NoHighlight | 26 | Revizyon değişikliklerini vurgulamak için renk kullanılmaz. |
| ByAuthor | 27 | Her yazarın revizyonları, önceden tanımlanmış yüksek kontrastlı renk setinden kendi vurgulama renklerini alır. |


## Örnekler



Bir oluşturulmuş çıktı belgesinde revizyonların görünümünün nasıl değiştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşile değiştirin.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Her revize edilmiş satırın solunda görünen çubuğu kaldırın.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
