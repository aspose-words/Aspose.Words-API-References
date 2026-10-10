---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::StoryType enum. Bir Word belgesinin metni hikayeler içinde depolanır. StoryType, C++'da bir hikayeyi tanımlar."
type: docs
weight: 117000
url: /tr/cpp/aspose.words/storytype/
---
## StoryType enum


Bir Word belgesinin metni hikayeler içinde depolanır. [StoryType](./) bir hikayeyi tanımlar.

```cpp
enum class StoryType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Varsayılan değer. Belgede böyle bir hikaye yoktur. |
| MainText | 1 | Belgenin ana metnini içerir, [Body](../body/) tarafından temsil edilir. |
| Footnotes | 2 | Dipnot metnini içerir, [Footnote](../../aspose.words.notes/footnote/) tarafından temsil edilir. |
| Endnotes | 3 | Sonnot metnini içerir, [Footnote](../../aspose.words.notes/footnote/) tarafından temsil edilir. |
| Comments | 4 | Belge yorumlarını (ek açıklamaları) içerir, [Comment](../comment/) tarafından temsil edilir. |
| Textbox | 5 | Şekil veya metin kutusu metnini içerir, [Shape](../../aspose.words.drawing/shape/) tarafından temsil edilir. |
| EvenPagesHeader | 6 | Çift sayfalı başlık metnini içerir, [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| PrimaryHeader | 7 | Birincil başlık metnini içerir. Başlık tek ve çift sayfalar için farklı olduğunda, tek sayfalı başlık metnini içerir. [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| EvenPagesFooter | 8 | Çift sayfalı altbilgi metnini içerir, [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| PrimaryFooter | 9 | Birincil altbilgi metnini içerir. Altbilgi tek ve çift sayfalar için farklı olduğunda, tek sayfalı altbilgi metnini içerir. [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| FirstPageHeader | 10 | İlk sayfa başlık metnini içerir, [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| FirstPageFooter | 11 | İlk sayfa altbilgi metnini içerir, [HeaderFooter](../headerfooter/) tarafından temsil edilir. |
| FootnoteSeparator | 12 | Dipnot ayırıcı metnini içerir. |
| FootnoteContinuationSeparator | 13 | Dipnot devam ayırıcı metnini içerir. |
| FootnoteContinuationNotice | 14 | Dipnot devam bildirimi ayırıcı metnini içerir. |
| EndnoteSeparator | 15 | Dipnot ayırıcı metnini içerir. |
| EndnoteContinuationSeparator | 16 | Dipnot devam ayırıcı metnini içerir. |
| EndnoteContinuationNotice | 17 | Dipnot devam bildirimi ayırıcı metnini içerir. |


## Örnekler



Bir düğümden tüm şekilleri nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir şekil eklemek için DocumentBuilder kullanın. Bu bir satır içi şekildir,
// bu, bir üst Paragraph'a sahiptir ve bu Paragraph, ilk bölümün Body'sunun bir alt düğümüdür.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Bu Body'nin alt paragraflarındaki tüm şekilleri silebiliriz.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
